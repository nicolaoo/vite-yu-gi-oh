<script>
import axios from 'axios'
import playCard from './playCard.vue'

export default {
    data() {
        return {
            cardImage: [],
        }
    },
    methods: {
        getCard() {
            axios.
                get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
                .then((res) => {
                    console.log(res.data.data)
                    this.cardImage = res.data.data
                })
        }
    },
    created() {
        this.getCard()
    },
    components: {
        playCard
    }
}

</script>

<template>
    <main>
        <div class="container">
            <div class="row">
                <div class="head-grid">
                    <h4>
                        Found 39 Cards
                    </h4>
                </div>
                <div class="grid">
                    <playCard v-for="(element, i) in cardImage" :key="i" :card-image="element" />
                </div>
            </div>
        </div>
    </main>
</template>
 
<style lang="scss" scoped>
main {
    background-color: darkorange;
}

.grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
}

.row {
    padding: 20px;

    .head-grid {
        background-color: rgb(19, 19, 26);
        padding: 10px 0;

        h4 {
            padding-left: 10px;
            color: white;
            text-transform: uppercase;
            font-size: 12px;
            line-height: 15px;
        }
    }
}
</style>