<template>
    <div>
        <div><button @click="toggle">Modal</button></div>
        <div>{{ text }}</div>
    </div>
</template>

<script>
export default {
    name: "App",
    data() {
        return {
            text: "Hola Vue",
        };
    },
    beforeCreate() {
        console.log("beforeCreate", this.$data, this.$el);
    },
    created() {
        console.log("Create", this.$data, this.$el);
    },
    mounted() {
        console.log("mounted", this.$data, this.$el);
    },
    beforeMount() {
        console.log("unmounted", this.$data, this.$el);
    },
    updated() {
        console.log("updated", this.$data, this.$el);
    },
    beforeUpdate() {
        console.log("beforeUpdate", this.$data, this.$el);
    },
    methods: {
        toggle() {
            this.text = "new text";
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
