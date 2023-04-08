<template>
    <div class="modal">
        <div class="modal-view">
            <thumbInModal :images="items" @selectedImg="showImage($event)"/>
            <div class="main-img-wrapper" >
                <img class="main-img" :src="image">
            </div>
            <div class="closingBtn">
            <button @click="closeModal">Close</button>
            </div>
        </div>
    </div>
</template>

<script>
import thumbInModal from '../gallery/thumbInModal.vue';
export default{
    name: "Modal",
    props: {
        image: {
            type: String,
            default: () => ""
        }
    },
    methods: {
        closeModal() {
            this.$emit("close", false);
        },
        showImage(url) {
            this.image = url;
        }
    },
    data() {
        return {
            items: [
                "https://img.freepik.com/free-photo/tulips-bouquet-pink-background-with-copyspace_24972-271.jpg?w=996&t=st=1679828190~exp=1679828790~hmac=4de0adf5a31b48bc6c5b800a4dab8b0fba44b4062c77298cf9d38e4de1b01378",
                "https://img.freepik.com/free-photo/beautiful-flowers-bouquet-with-copy-space_23-2149053793.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph",
                "https://img.freepik.com/premium-photo/pink-flowers-blooming-during-spring_260036-333.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph",
                "https://img.freepik.com/free-photo/arrangement-spring-flowers-with-copy-space_23-2148822273.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph",
                "https://img.freepik.com/free-photo/landscape-bow-bouquet-gift-outdoor_1304-3412.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph",
                "https://img.freepik.com/free-photo/floral-ornaments_23-2148134159.jpg?size=626&ext=jpg&ga=GA1.2.11231192.1675090670&semt=sph"
            ],
        };
    },
    components: { thumbInModal }
}
</script>
<style scoped>
.modal{
    display:flex;
    justify-content: center;
    position:absolute;
    top:0;
    left:0;
    width: 100vw;
    height: 100vh;
    background: rgba(55, 55, 55, 0.675);
}

.modal-view{
    background-color: white;
    width:800px;
    height: 600px;
    display: flex;
    flex-direction: row;
    position: absolute;
    top: 10vh;
    border: 0.5px solid darkgray;
}

.main-img{
    width:400px;
    height:400px;
}

.main-img-wrapper{
    margin:auto;
}

button{
    background-color: darkgray;
    color:white;
    border-radius: 7px;
    border: none;
    font-size:larger;
    margin: 5px;
}

button:hover{
    cursor:pointer;
}

.selected{
    border: 1px solid black
}
</style>