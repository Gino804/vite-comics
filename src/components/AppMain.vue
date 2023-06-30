<script>
export default {
    props: { comics: Array }
}
</script>

<template>
    <main>
        <section id="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="Jumbotron">
        </section>
        <section id="comics">
            <div class="container">
                <legend>CURRENT SERIES</legend>
                <div class="row">
                    <div v-for="comic in comics" :key="comic.thumb" class="column">
                        <div class="card">
                            <figure>
                                <img :src="comic.thumb">
                            </figure>
                            <h5>{{ comic.series }}</h5>
                        </div>
                    </div>
                </div>
            </div>
            <a href="#" class="button">LOAD MORE</a>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/vars' as *;

#jumbotron {
    height: 400px;

    img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: top;
    }
}

#comics {
    background-color: #1C1C1C;
    padding-bottom: 30px;

    legend {
        background-color: $blue;
        color: white;
        padding: 10px;
        width: 170px;
        text-align: center;
        font-weight: bold;
        transform: translate(0, -50%);
    }

    .row {
        display: flex;
        flex-wrap: wrap;

        .column {
            flex-basis: calc(100% / 6);

            .card {
                padding: 15px;

                figure {
                    width: 100%;
                    height: 160px;

                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                        object-position: top;
                    }
                }

                h5 {
                    color: white;
                    text-transform: uppercase;
                    margin-top: 10px;
                    font-weight: normal;
                }
            }

            &:first-child img,
            &:last-child img {
                transform: scale(1.45);
                clip-path: inset(0 31px 50px 31px);
                margin-top: 36px;
            }
        }
    }

    .button {
        background-color: $blue;
        color: white;
        font-weight: bold;
        display: block;
        margin: 0 auto;
        padding: 10px 0;
        text-align: center;
        width: 200px;
    }
}
</style>