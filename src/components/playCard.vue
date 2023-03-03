<script>
export default {
    data() {
        return {

        }
    },
    props: {
        cardImage: {
            type: Array,
            require: true,
        }
    }
}
</script>

<template>
    <div class="card">
        <figure>
            <img :src="cardImage.card_images[0].image_url" alt="">
        </figure>
        <div class="feature">
            <h5>{{ cardImage.name }} </h5>
            <p>{{ cardImage.type }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    padding: 5px;

    .feature {
        background-color: white;
        padding: 10px;

        h5 {
            text-align: center;
            color: darkorange;
            text-transform: uppercase;
            font-size: 10px;
        }

        p {
            text-align: center;
            padding-top: 12px;
        }
    }
}
</style>