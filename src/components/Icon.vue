<template>
    <svg class="icon" @click="$emit('click',$event)">
        <use :xlink:href="'#' + name"></use>
    </svg>
</template>

<script lang="ts">
    // import 一个目录
    const importAll = (requireContext: __WebpackModuleApi.RequireContext) => requireContext.keys().forEach(requireContext);
    try {
        importAll(require.context('../assets/icons', true, /\.svg$/));
    } catch (error) {
        console.log(error);
    }
    export default {
        name: 'Icon',
        props: ['name']
    };
</script>

<style lang="scss" scoped>
    .icon {
        width: 1em;
        height: 1em;
        vertical-align: -0.15em;
        overflow: hidden;
        fill: currentColor;
    }
</style>