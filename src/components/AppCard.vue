<script>
export default {
    name: "AppCard",
    props: {
        image: String,
        text: String
    }
}
</script>

<template>
    <!-- Card -->
    <div class="card">
        <!-- Card image -->
        <div class="card-image">
            <img :src="image" :alt="text">
        </div>
        <!-- Card title -->
        <div class="card-title">
            {{ text }}
        </div>
    </div>
</template>

<style scoped lang="scss">
.card {
    width: calc(100% / 6 - 20px);
    margin: 0 10px 40px;

    &-image {
        margin-bottom: 10px;

        img {
            height: 220px;
            width: 100%;
        }
    }

    &-title {
        color: white;
        text-align: left;
        font-weight: 500;
    }
}
</style>