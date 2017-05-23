<template>
    <div class="container" v-html="readme"></div>
</template>

<script>
    import readme from '../../../CLI.md';

    export default {
        layout: 'docs',
        computed: {
            readme() {
                return readme;
            }
        }
    };
</script>
