<template>
    <div>
        <Layout>
            <div class="tags">
                <router-link class="tag" :to="`/labels/edit/${tag.id}`" v-for="tag in tags" :key="tag.id">
                    <span>{{tag.name}}</span>
                    <Icon name="right"/>
                </router-link>
            </div>
            <div class="createTag-wrapper">
                <Button class="createTag" @click="createTag">新建标签</Button>
            </div>
        </Layout>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue';
    import {Component} from 'vue-property-decorator';
    import Button from '@/components/Button.vue';
    import {mixins} from 'vue-class-component';
    import TagHelper from '@/mixins/TagHelper';

    @Component({
        components: {Button},
    })
    export default class Labels extends mixins(TagHelper) {
        get tags(){
            return this.$store.state.tagList;
        }
        beforeCreate(){
            this.$store.commit('fetchTags')
        }
    }
</script>

<style lang="scss" scoped>
    .tags {
        background: white;
        font-size: 16px;
        padding-left: 16px;

        > .tag {
            min-height: 44px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: solid 1px #e6e6e6;

            svg {
                margin-right: 16px;
                width: 18px;
                height: 18px;
                color: #666;
            }
        }
    }

    .createTag {
        background: #767676;
        color: white;
        border: none;
        border-radius: 4px;
        height: 40px;
        padding: 0 16px;

        &-wrapper {
            text-align: center;
            margin-top: 28px;
            padding: 16px;
        }
    }
</style>