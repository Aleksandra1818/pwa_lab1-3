<template>
    <div class="nav">
    <NuxtLink class="nav-item" to="/">Main</NuxtLink>
    <NuxtLink class="nav-item" to="/about"> About</NuxtLink>
    <NuxtLink class="nav-item" to="/gallery"> Galeria</NuxtLink>
    </div>
</template>

<script>
export default {
  name: 'Navpage'
}
</script>

<style scoped>
.nav{
    display:flex;
    background-color: lightblue;
    flex-wrap: wrap;
    min-height: 50px;
    margin-left: 5px;

}

.nav-item{
    padding: 15px 5px 10px 5px;
    text-decoration: none;
    color: white;
}

.nav-item:hover{
    color: blanchedalmond;
}
</style>