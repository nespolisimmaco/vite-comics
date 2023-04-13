<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <!-- Container -->
        <div class="container">
            <!-- Content -->
            <div class="content">
                <!-- Logo -->
                <div class="logo">
                    <a href="#">
                        <img src="../assets/img/dc-logo.png" alt="DC logo">
                    </a>
                </div>
                <!-- Links -->
                <div class="header-links">
                    <ul class="header-list">
                        <li v-for="(link, index) in links" :class="link.current ? 'active' : ''">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <!-- End Content -->
        </div>
        <!-- End Container -->
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
    height: $header-height;
    .container {
        @include container();
        .content {
            @include flex();
            justify-content: space-between;
            align-items: center;
            .logo {
                img {
                    height: $header-height;
                    padding: 15px 0;
                }
            }
            .header-links {
                .header-list {
                    @include flex();

                    li {
                        list-style-type: none;
                        line-height: $header-height;
                        margin-right: 1.5rem;
                        font-size: .7rem;
                        font-weight: 600;
                        &.active {
                            border-bottom: 3px solid $primary-blue;
                            & a {
                                color: $primary-blue;
                            }
                        }
                        a {
                            text-decoration: none;
                            color: black;
                        }
                    }
                }
            }
        }
    }
}
</style>