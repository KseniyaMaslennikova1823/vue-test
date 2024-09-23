<template>
    <div class="app">
        <Header/>
        <Form/>
        <Footer/>
    </div>
</template>

<script>
import Header from "@/components/header.vue";
import Form from "@/components/form.vue";
import Footer from "@/components/footer.vue";

export default {
    components: {
        Header,
        Footer,
        Form
    },
}
</script>

<style lang="scss">
* {
    margin: 0;
    padding: 0;
}
</style>