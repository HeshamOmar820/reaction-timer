<template>
    <p> {{ score }} <span>مللي ثانيه</span></p> 
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return{
            rank: null,
        }
    },
    mounted() {
        if (this.score < 250 ){
            this.rank= '🚀🚀سريع فشخخخ'
        }else if (this.score < 800 ){
            this.rank= '👍🏻يجي منك'
        } else {
            this.rank= '🐌بطئ فشخخخ'
        }

}
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>