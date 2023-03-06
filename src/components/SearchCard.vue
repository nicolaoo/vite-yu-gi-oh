<script>
import store from '../store'
import PlayCard from './playCard.vue';

export default {

    data() {
        return {
            store,
            typeOptions: [
                "Effect Monster",
                "Flip Effect Monster",
                "Flip Tuner Effect Monster",
                "Gemini Monster",
                "Normal Monster",
                "Ritual Monster",
                "Spell Card",
                "Spirit Monster",
                "Toon Monster",
                "Trap Card",
                "Tuner Monster",
                "Union Effect Monster",
                'ciao'

            ]
        }
    }
}

</script>

<template>
    <div>
        <input @keyup.enter="$emit('onSearchName')" type="text" placeholder="inserici un nome" v-model="store.userNameCard">
    </div>
    <div>
        <select @change="$emit('onType')" v-model="store.selectType" id="">
            <option :value="PlayCard">-- type --</option>
            <option v-for="element in typeOptions" :value="element" :key="element">{{ element.toLowerCase() }}</option>
        </select>
    </div>
</template>

<style lang="scss"  scoped>
input,
select {
    padding: 8px;
    border-radius: 10px;
    margin: 10px 0;

    option {
        text-align: center;
    }
}
</style>