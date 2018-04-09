<template lang="html">
    <div>
        <Heador/>
        <Islider/>
        <Weifare/>
        <Activity/>
        <Service/>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Islider from "../ious/islider.vue"
import Weifare from "../ious/welfare.vue"
import Activity from "../ious/activity.vue"
import Service from "../ious/service.vue"
export default {
    components: {
        Heador,
        Footor,
        Navbar,
        Islider,
        Weifare,
        Activity,
        Service
    },
}
</script>
