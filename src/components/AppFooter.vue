<script>
export default {
    name: "AppFooter",
    data() {
        return {

        }
    }
}
</script>

<template>
    <footer>
        <!-- Footer top -->
        <div class="footer-top">
            <!-- Content -->
            <div class="top-content">
                <!-- Footer links and image -->
                <div class="top-footer-links">
                    <!-- Top footer links -->
                    <div class="links">
                        <!-- First column -->
                        <div class="column-links">
                            <h2>DC COMICS</h2>
                            <ul>
                                <li>
                                    <a href="#">Characters</a>
                                </li>
                                <li>
                                    <a href="#">Comics</a>
                                </li>
                                <li>
                                    <a href="#">Movies</a>
                                </li>
                                <li>
                                    <a href="#">TV</a>
                                </li>
                                <li>
                                    <a href="#">Games</a>
                                </li>
                                <li>
                                    <a href="#">Videos</a>
                                </li>
                                <li>
                                    <a href="#">News</a>
                                </li>
                            </ul>
                            <h2>SHOP</h2>
                            <ul>
                                <li>
                                    <a href="#">Shop DC</a>
                                </li>
                                <li>
                                    <a href="#">Shop DC Collectibles</a>
                                </li>
                            </ul>
                        </div>
                        <!-- Second column -->
                        <div class="column-links">
                            <h2>DC</h2>
                            <ul>
                                <li>
                                    <a href="#">Terms Of Use</a>
                                </li>
                                <li>
                                    <a href="#">Privacy policy (New)</a>
                                </li>
                                <li>
                                    <a href="#">Ad Choices</a>
                                </li>
                                <li>
                                    <a href="#">Advertising</a>
                                </li>
                                <li>
                                    <a href="#">Jobs</a>
                                </li>
                                <li>
                                    <a href="#">Subscriptions</a>
                                </li>
                                <li>
                                    <a href="#">Talent Workshops</a>
                                </li>
                                <li>
                                    <a href="#">CPSC Certificates</a>
                                </li>
                                <li>
                                    <a href="#">Ratings</a>
                                </li>
                                <li>
                                    <a href="#">Shop Help</a>
                                </li>
                                <li>
                                    <a href="#">Contact Us</a>
                                </li>
                            </ul>
                        </div>
                        <!-- Third column -->
                        <div class="column-links">
                            <h2>SITES</h2>
                            <ul>
                                <li>
                                    <a href="#">DC</a>
                                </li>
                                <li>
                                    <a href="#">MAD Magazine</a>
                                </li>
                                <li>
                                    <a href="#">DC Kids</a>
                                </li>
                                <li>
                                    <a href="#">TDC UniverseV</a>
                                </li>
                                <li>
                                    <a href="#">DC Power Visa</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <!-- End Top footer links -->
                </div>
                <!-- End Footer links and image -->
            </div>
            <!-- End Content -->
        </div>
        <!-- Footer bottom -->
        <div class="footer-bottom">
            <!-- Content -->
            <div class="bottom-content">
                <!-- Sign-up button -->
                <a class="sign-up-button" href="#">SIGN-UP NOW!</a>
                <!-- Social links -->
                <div class="social-links">
                    <h2>FOLLOW US</h2>
                    <ul>
                        <li>
                            <a href="#"><img src="../assets/img/footer-facebook.png" alt="Facebook"></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-twitter.png" alt="Twitter"></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-youtube.png" alt="Youtube"></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-pinterest.png" alt="Pinterest"></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-periscope.png" alt="Periscope"></a>
                        </li>
                    </ul>
                </div>
            </div>
            <!-- End Content -->
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.footer-top {
        background-image: url(../assets/img/footer-bg.jpg);    
        .top-content {
            @include container();
            .top-footer-links {
                padding: 2rem 0 3rem;
                background-image: url(../assets/img/dc-logo-bg.png);
                background-repeat: no-repeat;
                background-position: right;
                .links {
                    @include flex();
                    width: 40%;
                    .column-links {
                        width: calc(100% / 3);
                        h2 {
                            color: white;
                            margin-bottom: 1rem;
                        }
                        li {
                            list-style-type: none;
                            font-size: .8rem;
                            margin: 8px 0;
    
                            a {
                                color: grey;
                                text-decoration: none;
                            }
                        }
                    }
                }
            }
        }
}
.footer-bottom {
    background-color: $footer-grey;
    height: $header-height;
    .bottom-content {
        @include container();
        @include flex();
        height: 100%;
        justify-content: space-between;
        align-items: center;
        .sign-up-button {
            border: 2px solid $primary-blue;
            padding: 10px;
            color: white;
            text-decoration: none;
        }
        .social-links {
            @include flex();
            h2 {
                color: $primary-blue;
                margin-right: 1rem;
            }
            ul {
                @include flex();
                li {
                    list-style-type: none;
                    margin: 0 10px;
                }
            }
        }
    }
}
</style>