<template>
<article class="">
    <Slider :items="items" :cname="$style.slider" />
    <section :class="$style.list">
        <div :class="$style.item" v-for="item in enters" :key="item.img">
            <router-link :to="{ name: item.href }">
                <img :src="item.img" alt="item.title" />
                <h4 v-if="item.title == '抢钢镚'" style="color:red;">{{ item.title }}</h4>
                <h4 v-else>{{ item.title }}</h4>
            </router-link>
        </div>
    </section>
</article>
</template>
<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18349/345/1321205947/50059/7d0d9cbd/5ac47fceN0e377ff7.jpg?width=750&height=320"
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18880/271/1296475191/69529/c4010ed3/5ac47f9aNfa279aba.jpg?width=750&height=320"
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18919/93/1298065818/30323/f00c58d0/5ac47ff6Ned451d29.jpg?width=750&height=320"
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t19186/155/1303007381/55081/50c0b4d6/5ac4801dN6206e47e.jpg?width=750&height=320"
            }],
            enters: [{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                title: "优惠卷"
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                title: "领红包"
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                title: "抢钢镚"
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                title: "白条提额"
            }],
        }
    },
}
</script>
<style lang="scss" module>
    @import "../../css/element.scss";
    .slider {
        margin-top: 120px;
        img{
            width: 100%;
        }
    }
    .list{
        @include list(row);
        background: #fff;
        padding-top: 40px;
        justify-content: space-around;
        a{
            text-decoration: none;
        }
        .item{
            text-align: center;
            height: 140px;
            img{
                display: inline-block;
                width: 90px;
                height: 90px;
            }
            h4{
                font-size: 26px;
                margin-top: 6px;
                color: #666;

            }
        }
    }
</style>
