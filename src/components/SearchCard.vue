<script>
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
        <input type="text" placeholder="inserici un nome" v-model="userNameCard">
    </div>
</template>

<style lang="scss"  scoped>
input {
    padding: 8px;
    border-radius: 10px;
    margin: 10px 0;
}
</style>