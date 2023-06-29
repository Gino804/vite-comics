<script>
export default {
    data() {
        return {
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    },
}
</script>

<template>
    <header>
        <div class="container">
            <nav>
                <figure>
                    <img src="../assets/img/dc-logo.png" alt="DC Logo">
                </figure>
                <ul>
                    <li v-for="link in links" :key="link.text"><a :href="link.url" :class="{ 'active': link.current }">{{
                        link.text }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped>
header {
    height: 150px;
}

.container {
    height: 100%;
}

figure {
    display: flex;
    align-items: center;
}

nav {
    display: flex;
    justify-content: space-between;
    height: 100%;
}

ul {
    display: flex;
    height: 100%;
}

li {
    margin: 0 20px;
    height: 100%;
}

a {
    text-transform: uppercase;
    color: rgb(80, 78, 78);
    font-size: 14px;
    font-weight: bold;
    height: 100%;
    display: flex;
    align-items: center;
}

li:hover a {
    color: #0282F9;
    border-bottom: 3px solid #0282F9;
}

.active {
    color: #0282F9;
    border-bottom: 3px solid #0282F9;
}
</style>