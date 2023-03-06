<script>
import axios from 'axios'
import playCard from './playCard.vue'
import store from '../store'
import SearchCard from './SearchCard.vue'

export default {
    data() {
        return {
            // cardImage: [],
            store,

        }
    },
    methods: {
        getCard() {
            const search = this.store.userNameCard
            const select = this.store.selectType
            console.log('quetso è search: ', search)

            axios.
                get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0', {
                    params: {
                        fname: search,
                        type: select
                    }
                })
                .then((res) => {
                    console.log(this.store.cardImage)
                    this.store.cardImage = res.data.data
                }).catch((error) => {
                    console.log(error)
                    this.store.cardImage = []

                })


        }
    },
    created() {
        this.getCard()
    },
    components: {
        playCard,
        SearchCard,
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
                <div class="container">
                    <div class="input-bar">
                        <SearchCard @onSearchName="getCard" @onType="getCard" />

                        {{ store.userNameCard }}
                        {{ store.selectType }}
                    </div>

                </div>

                <div class="grid" v-if="store.cardImage.length > 0">
                    <playCard v-for="(element, i) in store.cardImage" :key="i" :card-image="element" />
                </div>
                <div v-else class="grid-error">
                    prova a cercare un'altro nome!!!!
                </div>
            </div>
        </div>
    </main>
</template>
 
<style lang="scss" scoped>
.input-bar {
    display: flex;
    align-items: center;
    gap: 20px;
    font-size: 20px;
}

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

    .grid-error {
        font-size: 25px;
        height: 100vh;
        display: flex;
        align-items: start;
        justify-content: center;
        text-transform: uppercase;
        padding-top: 40px;
    }
}
</style>