<template>
    <div>
        <h2>About</h2>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse
            aperiam suscipit similique quaerat non, officia culpa eos quas
            numquam dignissimos dolorem distinctio maiores dolores quasi quos
            qui maxime illum?
        </p>
        <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque
            labore eos dolor unde esse. Ab ratione sapiente obcaecati quod sint
            odit labore hic dolor dolorem voluptatibus itaque, maxime voluptatum
            temporibus?
        </p>
    </div>
</template>

<script setup>
const { data } = await useFetch("/api/currency/GBP");
// data not used, was just written out to the screen for tutorial purposes.
</script>

<style scoped>
h2 {
    margin-bottom: 1.25rem;
    font-size: 2rem;
}
p {
    margin: 1.25rem 0;
}
</style>
