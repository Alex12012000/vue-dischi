<template>
    <div class="card">
        <img :src="detail.poster" :alt="detail.title">
        <h3>{{detail.title}}</h3>
        <span>{{detail.author}}</span>
        <span>{{detail.year}}</span>
    </div>
</template>

<script>
export default {
    name: 'MusicCard',
    props: {
        detail: Object
    }
}
</script>


<style lang="">
    
</style>