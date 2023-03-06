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
            console.log('quetso è search: ', search)

            axios.
                get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0', {
                    params: {
                        fname: search,
                    }
                })
                .then((res) => {
                    console.log(this.store.cardImage)
                    this.store.cardImage = res.data.data
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
                        <SearchCard @onSearchName="getCard" />

                        {{ store.userNameCard }}

                    </div>

                </div>

                <div class="grid">
                    <playCard v-for="(element, i) in store.cardImage" :key="i" :card-image="element" />
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
}
</style>