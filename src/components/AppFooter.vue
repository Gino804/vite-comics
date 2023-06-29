<template>
    <footer>
        <section id="links">
            <div class="container">
                <div>
                    <h3>DC COMICS</h3>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>
                    <h3>SHOP</h3>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>
                <div>
                    <h3>DC</h3>
                    <ul>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy Policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>
                <div>
                    <h3>SITES</h3>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
            </div>
        </section>
        <section id="socials">
            <div class="container">
                <a href="#" class="button"> SIGN-UP NOW! </a>
                <div>
                    <h3>FOLLOW US</h3>
                    <img src="../assets/img/footer-facebook.png">
                    <img src="../assets/img/footer-twitter.png">
                    <img src="../assets/img/footer-youtube.png">
                    <img src="../assets/img/footer-pinterest.png">
                    <img src="../assets/img/footer-periscope.png">
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/vars' as *;
@use '../assets/scss/partials/mixins' as *;

#links {
    @include background_img_no_repeat('../assets/img/footer-bg.jpg');
    background-size: cover;
}

#links>.container {
    display: flex;
    padding: 30px 0;
    @include background_img_no_repeat('../assets/img/dc-logo-bg.png');
    background-position: right;
}

#links>.container>div {
    margin-right: 20px;
}

#links h3 {
    color: white;
}

a {
    color: #89908F;
    font-size: 12px;
}

#socials {
    background-color: #303030;
    height: 120px;
}

#socials>.container {
    height: 100%;
    @include flex_between;
    align-items: center;
}

.button {
    border: 2px solid $blue;
    padding: 10px;
    color: white;
    font-weight: bold;
    font-size: 17px;
}

#socials h3 {
    color: $blue;
}

#socials>.container>div {
    @include flex_center('cross');
}

#socials img {
    margin-left: 20px;
}
</style>