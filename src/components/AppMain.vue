<script>
export default {
    data() {
        return {

        }
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
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                    <div class="card">
                        <figure>
                            <img src="https://static-it.gamestop.it/images/products/301603/3max.jpg" alt="">
                        </figure>
                        <div class="feature">
                            <h5>'A' cell breending device </h5>
                            <p>Alien</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>
 
<style lang="scss" scoped>
main {
    background-color: darkorange;
}

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