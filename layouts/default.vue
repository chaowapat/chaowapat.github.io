<template>
    <div>
        <Topbar></Topbar>
        <b-container class="sk-container">
            <Nuxt></Nuxt>
        </b-container>
    </div>
</template>

<script>
import Topbar from '../components/Topbar.vue';

export default {
    components: { Topbar },
    setup() {
        return {};
    },
}
</script>

<style lang="css" scoped>
 .sk-container {
     margin-top: 40px;
 }

</style>