<template>
    <nav>
        <router-link to="/money" class="item" active-class="selected">
            <Icon name="money"></Icon>
            记账
        </router-link>
        <router-link to="/labels" class="item" active-class="selected">
            <Icon name="label"></Icon>
            标签
        </router-link>
        <router-link to="/statistics" class="item" active-class="selected">
            <Icon name="statistics"></Icon>
            统计
        </router-link>
    </nav>
</template>

<script lang="ts">

    export default {
        name: 'Nav'
    };
</script>

<style lang="scss" scoped>
    nav {
        display: flex;
        box-shadow: 0 0 3px rgb(0, 0, 0, 0.25);
        flex-direction: row;
        font-size: 12px;

        > .item {
            padding: 2px 0;
            display: flex;
            width: 33.3333333%;
            justify-content: center;
            align-items: center;
            flex-direction: column;

            .icon {
                width: 32px;
                height: 32px;
            }
        }
        > .item.selected{
            color: hotpink;
        }

    }
</style>