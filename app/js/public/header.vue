<template>
<div :class="$style.header">
    <span :class="$style.left">
                <!-- 真实项目不能写死，需要使用路由 -->
                <em>注册</em>&nbsp;|&nbsp<em>登录</em>
            </span>
    <btn :class="$style.btnDownload">APP下载</btn>

</div>
</template>
<script>
import btn from "../core/btn.vue"
export default {
    // 通过某个 Vue 实例/组件的实例选项 components
    // 注册仅在其作用域中可用的组件
    components: {
        btn,
    },
}
</script>
<style lang="scss" module>
.header {
    height: 100px;
    line-height: 100px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    font-size: 32px;
    color: #666;
    background: #fff url("//m.jr.jd.com/spe/qyy/main/images/jr-logo.png") center center no-repeat;
    background-size: auto 50%;
    z-index: 100;
    .left {
        font-size: 28px;
        height: 30px;
        line-height: 30px;
        margin: 17px 0 0 18px;
    }
    .btnDownload {
        float: right;
        font-size: 24px;
        border-width: 0;
        height: 56px;
        line-height: 56px;
        min-width: 120px;
        padding: 0;
        border-radius: 4px;
        margin: 28px 24px 0 0;
    }
}
</style>
