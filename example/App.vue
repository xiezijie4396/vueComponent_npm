<template>
    <div id="app">
        <demo />
    </div>
</template>

<script>
import demo from "@/components/demo.vue";

export default {
    name: "App",
    components: {
        demo
    }
};
</script>

<style>
* {
    padding: 0;
    margin: 0;
}
</style>