<template lang="html">
    <section class="panel">
        <h4> - {{ title }} - </h4>
        <!-- 插槽，插入内容 -->
        <slot/>
    </section>
</template>
<script>
export default {
    // 父组件通过 props 向下传递数据给子组件
    props: {
        cname: {
            type: String,
            default: "",
        },
        title:{
            type: String,
            default: "",
        },
    },
    data() {
        return {
            panelClass: "panel",
        }
    }
}
</script>
<style lang="scss">
    @import "../../css/element.scss";
    .panel{
        @include panel;
    }
</style>
