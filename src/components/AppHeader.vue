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

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

header {
    height: 150px;
}

.container {
    height: 100%;
}

figure {
    @include flex_center('cross');
}

nav {
    @include flex_between;
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
    @include flex_center('cross');
}

li:hover a {
    @include header_link_active;
}

.active {
    @include header_link_active;
}
</style>