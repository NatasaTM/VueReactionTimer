<template>
<p class="rTime">Reaction time: {{ score }}</p>
<p class="rank">Rank: {{ rank }}</p>
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
.rTime {
    font-weight: bold;
}
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>