<template>
    <div style="display: none">
        <div :id="id"
             :class="{ modal:true,fade: fade, in: animateModal || !fade }"
             style="display: block"
             @click="onClickOut($event)">
            <div :class="['modal-dialog','modal-'+size]" role="document" style="z-index: 9999">
                <div class="modal-content">
                    <div class="modal-header">
                        <slot name="modal-header"></slot>
                    </div>
                    <div class="modal-body">
                        <slot name="modal-body"></slot>
                    </div>
                    <div class="modal-footer">
                        <slot name="modal-footer"></slot>
                    </div>
                </div>
            </div>
        </div>
        <div class="modal-backdrop" :class="{ fade: fade, in: animateBackdrop || !fade }"></div>
    </div>
</template>

<script>
    import {csstransitions} from '../utils/helpers.js'

    export default {

        data() {
            return {
                animateBackdrop: false,
                animateModal: false,
            }
        },

        computed: {
            _transition_duration(){
                // This is directly linked to the bootstrap animation timing in _modal.scss
                // For browsers that do not support transitions like IE9 just change slide immediately
                // Also this applies to SSR conditions
                if (!csstransitions()) return 0;
                return this.transition_duration;
            }
        },

        props: {
            id: {
                type: String,
                default: 'default'
            },
            size: {
                type: String,
                default: 'md'
            },
            fade: {
                type: Boolean,
                default: true
            },
            closeOnBackdrop: {
                type: Boolean,
                default: true,
            },
            transition_duration: {
                type: Number,
                default: 300,
            }
        },

        methods: {
            show() {
                this.$el.style.display = 'block';
                this._body = document.querySelector('body');
                const _this = this;

                // Wait for the display block, and then add class "in" class on the modal
                this._modalAnimation = setTimeout(() => {
                    this.animateBackdrop = true;
                    this._modalAnimation = setTimeout(() => {
                        this._body.classList.add('modal-open');
                        this.animateModal = true;
                        this.$root.$emit('shown::modal', this.id)
                    }, (_this.fade) ? this._transition_duration : 0)
                }, 0);
            },

            hide() {
                const _this = this;
                // First animate modal out
                this.animateModal = false;
                this._modalAnimation = setTimeout(() => {
                    // wait for animation to complete and then hide the backdrop
                    _this.animateBackdrop = false;
                    this._modalAnimation = setTimeout(() => {
                        _this._body.classList.remove('modal-open');
                        // no hide the modal wrapper
                        _this.$el.style.display = 'none';
                        _this.$root.$emit('hidden::modal', this.id)
                    }, (_this.fade) ? this._transition_duration : 0)
                }, (_this.fade) ? this._transition_duration : 0)
            },

            onClickOut(e) {
                // If backdrop clicked, hide modal
                if (this.closeOnBackdrop && e.target.id && e.target.id === this.id) {
                    this.hide()
                }
            },

        },

        mounted() {
            // Support for esc key press
            document.addEventListener('keydown', (e) => {
                const key = e.which || e.keyCode;
                if (key === 27) { // 27 is esc
                    this.hide()
                }
            })
        },

        destroyed() {
            clearTimeout(this._modalAnimation)
        },
    }

</script>
