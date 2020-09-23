<template>
    <div>
        <h2>{{tweet.tweet}}</h2>
        <h2>{{tweet.Name}}</h2>
        <h2>{{tweet.date}}</h2>

    </div>
</template>

<script>
import PageFooter from './components/page-footer.vue'
export default {
     name: "page-footer"
}
</script>
<style lang="stylus" scoped>

</style>

<style scoped>
.page-footer {
    display: grid;
    justify-items: center;
    align-items: center;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;

}
</style>