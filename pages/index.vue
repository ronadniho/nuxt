<template>
    <div id="home">
        home
    </div>
</template>


<script>
export default {
    async asyncData({ $axios }) {
        return $axios
        .get(`/api/web/check_price/getSystemDate`)
        .then(res => {
            console.log('-----')
            console.log(res.data)
            return {
                date:res.data
            }
        })
        .catch(e => {
            error({ statusCode: 404, message: 'Post not found' })
        })
    },
    name:'home',
    data(){
        return {
            date:''
        }
    },
    mounted(){
        console.log(this.date)
    }

}
</script>

<style lang="css">
    
</style>