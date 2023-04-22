<template>
    <div class="main-wrap">
        <h1 class="colorRed">About</h1>
        <div class="alert">
            <button @click="showInfo">Kliknij mnie</button>
        </div>
        <BigImage image="https://img.freepik.com/free-photo/tulips-bouquet-pink-background-with-copyspace_24972-271.jpg?w=996&t=st=1679828190~exp=1679828790~hmac=4de0adf5a31b48bc6c5b800a4dab8b0fba44b4062c77298cf9d38e4de1b01378"/>
        <Thumb image1="https://img.freepik.com/free-photo/tulips-bouquet-pink-background-with-copyspace_24972-271.jpg?w=996&t=st=1679828190~exp=1679828790~hmac=4de0adf5a31b48bc6c5b800a4dab8b0fba44b4062c77298cf9d38e4de1b01378"
        image2="https://img.freepik.com/free-photo/beautiful-flowers-bouquet-with-copy-space_23-2149053793.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
        image3="https://img.freepik.com/premium-photo/pink-flowers-blooming-during-spring_260036-333.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
        image4="https://img.freepik.com/free-photo/arrangement-spring-flowers-with-copy-space_23-2148822273.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
        image5="https://img.freepik.com/free-photo/landscape-bow-bouquet-gift-outdoor_1304-3412.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
        image6="https://img.freepik.com/free-photo/floral-ornaments_23-2148134159.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
        />
    </div>

</template>
<script>
import BigImage from '~/components/gallery/bigImage.vue';
import Thumb from '~/components/gallery/thumb.vue';
import TopNav from '~/components/TopNav.vue';
export default {
    name: "AboutPage",
    components: { TopNav, BigImage, Thumb },

    methods: {
        showInfo: () => alert('Witaj')
    }
}
</script>
<style scoped>
.colorRed{
    color: red;
    text-align: center;
}
.main-wrap{
    justify-content: center;
    flex-wrap: wrap;
}

.alert{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    padding-bottom: 10px;
}
</style>