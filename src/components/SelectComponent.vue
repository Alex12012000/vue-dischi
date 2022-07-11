<template>
    <div>
        <select v-model="selected" @change="$emit('changeValue', selected)">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Metal">Metal</option>
            <option value="Jazz">Jazz</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "SelectComponent",
    data() {
        return {
            selected: "All",
        }
    },
}
</script>

<style lang="scss">
    
</style>