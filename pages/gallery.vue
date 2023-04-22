<template>
    <div class="main-wrap">
        <div class="gallery-wrap">
        <BigImage :image="bigImg" @rm="runModal($event)"/>
        <Thumb :images="items" @selectedImg="showImage($event)"/>
        <Modal1 v-show="showModal" :image="bigImg" @close="runModal($event)"/>
        </div>
    </div>

</template>
<script>
import BigImage from '~/components/gallery/bigImage.vue';
import Thumb from '~/components/gallery/thumb.vue';
import Modal1 from '~/components/modals/modal1.vue';
import TopNav from '~/components/TopNav.vue';

export default {
    name: 'Gallery',
    components: { TopNav, BigImage, Thumb, Modal1 },
    data(){
        return{
            items:[
                'https://img.freepik.com/free-photo/tulips-bouquet-pink-background-with-copyspace_24972-271.jpg?w=996&t=st=1679828190~exp=1679828790~hmac=4de0adf5a31b48bc6c5b800a4dab8b0fba44b4062c77298cf9d38e4de1b01378',
                'https://img.freepik.com/free-photo/beautiful-flowers-bouquet-with-copy-space_23-2149053793.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph',
                'https://img.freepik.com/premium-photo/pink-flowers-blooming-during-spring_260036-333.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph',
                'https://img.freepik.com/free-photo/arrangement-spring-flowers-with-copy-space_23-2148822273.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph',
                'https://img.freepik.com/free-photo/landscape-bow-bouquet-gift-outdoor_1304-3412.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph',
                'https://img.freepik.com/free-photo/floral-ornaments_23-2148134159.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph'

            ],
            bigImg:'https://img.freepik.com/free-photo/tulips-bouquet-pink-background-with-copyspace_24972-271.jpg?w=996&t=st=1679828190~exp=1679828790~hmac=4de0adf5a31b48bc6c5b800a4dab8b0fba44b4062c77298cf9d38e4de1b01378',
            showModal : false

        }
    },
    methods: {
        showImage(url) {
            this.bigImg = url
        },
        runModal(e){
            this.showModal = e
        }
    }

}
</script>
<style scoped>
.main-wrap{
    justify-content: center;
    flex-wrap: wrap;

}

.gallery-wrap{
    margin-top: 20px;
}

</style>