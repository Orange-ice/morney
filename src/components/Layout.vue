<template>
    <div class="nav-wrapper" :class="classPrefix && `${classPrefix}-wrapper`">
        <div class="content" :class="classPrefix && `${classPrefix}-content`">
            <slot></slot>
        </div>
        <Nav></Nav>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Layout',
        props:['classPrefix']
    };
</script>

<style lang="scss" scoped>
    .nav-wrapper {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .content {
        overflow: auto;
        flex-grow: 1;
    }
</style>