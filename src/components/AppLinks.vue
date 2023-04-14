<script>
export default {
    name: "AppLinks",
    data() {
        return {
            links: [
                {
                    icon: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS"
                },
                {
                    icon: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE"
                },
                {
                    icon: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION"
                },
                {
                    icon: "buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR"
                },
                {
                    icon: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA"
                }
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <!-- Links with icons -->
    <div class="links">
        <!-- Container -->
        <div class="container">
            <!-- Content -->
            <div class="content">
                <ul>
                    <li v-for="(link, index) in links" class="link" :key="index">
                        <a href="#">
                            <img :src="getImagePath(link.icon)" :alt="link.text">
                            <div>{{ link.text }}</div>
                        </a>
                    </li>
                </ul>
            </div>
            <!-- End Content -->
        </div>
        <!--End Container -->
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as *;

.links {
    background-color: $primary-blue;
    color: white;
    padding: 2.5rem 0;
}

.container {
    @include container();
}

.content {
    ul {
        @include flex();
        justify-content: space-around;
    }
}

.link {
    list-style-type: none;

    a {
        text-decoration: none;
        color: inherit;
        @include flex();
        align-items: center;

        img {
            height: 40px;
            margin-right: 1rem;
        }
    }
}
</style>