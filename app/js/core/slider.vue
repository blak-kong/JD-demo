<template>
<section :class="cname">
    <swiper :options="options" :not-next-tick="options.notNextTick">
        <swiper-slide v-for="item in items" :key="item.href">
            <router-link :to="{ name: item.href }">
                <img :src="item.src" alt="" />
            </router-link>
        </swiper-slide>
        <!-- v-if="options.pagination判断是否有指示器 -->
        <div class="swiper-pagination" v-if="options.pagination" slot="pagination" />
    </swiper>
</section>
</template>
<script>
import {
    swiper,
    swiperSlide
} from "vue-awesome-swiper"

export default {
    components: {
        swiper,
        swiperSlide
    },
    // 父组件通过 props 向下传递数据给子组件
    // 子组件通过 events 给父组件发送消息
    props: {
        cname: {
            type: String,
            default: "",
        },
        options: {
            type: Object,
            default () {
                return {
                    autoplay: true, // 自动播放
                    loop: true, // 循环
                    pagination: { //轮播指示器
                        el: ".swiper-pagination",
                    },
                    notNextTick: false, //点击事件
                }
            },
        },
        items:{ //轮播图数组
            type:Array,
            default(){
                return [] //{href:'', src:''}
            },
        },
    }
}
</script>
<style lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>
