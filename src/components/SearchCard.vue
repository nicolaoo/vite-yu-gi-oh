<script>
import store from '../store'

export default {

    data() {
        return {
            store
        }
    }
}

</script>

<template>
    <div>
        <input @keyup.enter="$emit('onSearchName')" type="text" placeholder="inserici un nome" v-model="store.userNameCard">
    </div>
</template>

<style lang="scss"  scoped>
input {
    padding: 8px;
    border-radius: 10px;
    margin: 10px 0;
}
</style>