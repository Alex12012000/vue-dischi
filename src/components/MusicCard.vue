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


<style lang="scss" scoped>
    .card {
        padding: 10px;
        margin: 20px 0;
        background-color: #2e3a46;
        width: calc((100% / 5) - 15px); 
        text-align: center;
        h3 {
            padding: 15px 0;
            text-transform: uppercase;
            color: white;
        }
        span {
            display: block;
            margin: 5px 0;
            color: grey;
        }
    }
</style>