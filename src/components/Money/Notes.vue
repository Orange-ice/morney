<template>
    <div class="notes">
        <label>
            <span class="name">备注</span>
            <input type="text" placeholder="在这里添加备注">
        </label>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'Notes'
    };
</script>

<style lang="scss" scoped>
    .notes {
        font-size: 14px;
        background-color: #f5f5f5;
        padding-left: 16px;
        display: flex;
        align-items: center;

        .name {
            padding-right: 16px;
        }

        input {
            height: 64px;
            flex-grow: 1;
            background-color: transparent;
            border: none;
            padding-right: 16px;
        }
    }
</style>