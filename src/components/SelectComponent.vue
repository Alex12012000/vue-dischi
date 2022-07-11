<template>
    <div class="select-bar">
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

<style lang="scss" scoped>
    .select-bar {
        padding-top: 20px;
        text-align: center;
        select {
            padding: 5px 0;
            padding-right: 20px;
            padding-left: 5px;
            border-radius: 10px;
            border: 1px solid #2e3a46;
            text-align: left;
            background-color: #1e2d3b;
            color: white;
        }
    }
</style>