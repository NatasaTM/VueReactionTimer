<template>
<div class="block">Reaction time: {{ score }}</div>
<p>Rank: {{ rank }}</p>
</template>

<script>
export default{
props: ['score'],
data(){
    return {
        rank: null
    }
},
mounted(){
    if(this.score < 250){
        this.rank = 'Ninja fingers'
    } else if(this.score < 400){
        this.rank = 'Rapid Reflexes'
    }else{
        this.rank = "Snail pace"
    }
}
}
</script>

<style>
.block {
    width: 400px;
    border-radius: 20px;
    background: #0faf87;
    color: white;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}
</style>