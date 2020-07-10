<template>
    <div class="nav-wrapper">
        <div class="content">
            money
        </div>
        <Nav></Nav>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Money',
    };
</script>

<style lang="scss" scoped>
    .nav-wrapper {
        border: solid 1px green;
        display: flex;
        flex-direction: column;
        height: 100vh;
    }
    .content{
        overflow: auto;
        flex-grow: 1;
        border: solid 1px blue;
    }
</style>