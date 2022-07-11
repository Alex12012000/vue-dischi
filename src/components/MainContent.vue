<template>
    <div class="container">
        <SelectComponent @changeValue="selectedGenre"/>
        <div class="content" >
            <MusicCard v-for="cd in filterByGenre" :key="cd.id" :detail=" cd"/>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import MusicCard from './MusicCard.vue'
import SelectComponent from './SelectComponent.vue'

export default {
    name: 'MainContent',
    components: {
        MusicCard,
        SelectComponent
    },

    data() {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            cdArray: [],
            currentGenre: 'All'
        }
    },

    computed: {
        filterByGenre() {

            if(this.currentGenre === 'All') {
                return this.cdArray
            } else {
                return this.cdArray.filter(el => {
                    return el.genre.includes(this.currentGenre)
                })
            }
        }
            
    },

    methods: {
        getMusicInfo(){
            axios.get(this.url).then(result => {
                this.cdArray = result.data.response;
            })
        },
        
        selectedGenre(genre) {
            this.currentGenre = genre;
            console.log(this.currentGenre)
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