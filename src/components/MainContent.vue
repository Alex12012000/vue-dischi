<template>
    <div class="container">
        <div class="content">
            <MusicCard v-for="cd, index in cdArray" :key="index" :detail="cd"/>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import MusicCard from './MusicCard.vue'

export default {
    name: 'MainContent',
    components: {
        MusicCard
    },
    data() {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            cdArray: [],
        }
    },
    methods: {
        getMusicInfo(){
            axios.get(this.url).then(result => {
                this.cdArray = result.data.response;
            })
        }
    },
    mounted() {
        this.getMusicInfo()
    } 
        
    
}
</script>

<style lang="scss">
    .content {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>