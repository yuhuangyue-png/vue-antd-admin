<template>
    <div class="public">
        <a-button type="primary" @click="goBack" style="margin-right: 20px;">
        <a-icon type="left" />Backward
      </a-button>
        <a-select v-model="option" style="width: 120px" @change="handleChange">
            <a-select-option v-for="item in list" :key="item">
                {{ item }}
            </a-select-option>
        </a-select>
    </div>
</template>
<script>
export default {
    name: 'PublicPage',
    data() {
        return {
            list: ['a1', 'a2', 'a3'],
            option: undefined
        }
    },
    methods: {
        handleChange(value) {
            console.log(value)
        },
        goBack() {
            window.history.back(-1)
            console.log(window.history)
        }
    }
}
</script>

<style lang="less" scoped>
.public{
    margin: 5% 5%;
}
</style>