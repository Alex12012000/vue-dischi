<template>
    
    <header>
        <div class="logo">
            <img src="../assets/logo.png" alt="logo">
        </div>
    </header>

</template>


<script>
export default {
    name: 'PageHeader',
}
</script>


<style lang="scss">
    header {
        height: 80px;
        background-color: #2e3a46;

        .logo {
            display: flex;
            height: 100%;
            align-items: center;
            margin: 0 20px;
            img {
                width: 55px;
                height: 55px;
            }
        }
    }
</style>