<script>
export default {
    name: "AppMain",
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h2>--> Content goes here &lt;--</h2>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
main {
    background-color: black;
    .container {
        @include container();
        padding: 2.5rem 0;
        h2 {
            color: white;
        }
    }
}
</style>