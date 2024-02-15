<script>
export default {
    data() {
        return {
            photos: [],
        }
    },
    mounted() {
        this.getPhotos();
    },
    methods: {
        async getPhotos() {
            try {
                const response = await fetch("https://jsonplaceholder.typicode.com/photos")
                console.log(response);
                this.photos = await response.json();
            } catch (error) {
                console.log(error);
            }
        }
    },
}
</script>

<template>
    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-4 gap-8">
        <div v-for="photo in photos" :key="photo.i">
            <img :src="photo.url" alt="Photo">
            <p>{{photo.title}}</p>
        </div>
    </div>
</template>