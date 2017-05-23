<template>
    <div class="container" v-html="readme"></div>
</template>

<script>
    import readme from '../../../SETUP.md';

    export default {
        layout: 'docs',
        computed: {
            readme() {
                return readme;
            }
        }
    };
</script>
