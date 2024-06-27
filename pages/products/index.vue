<template>
    <div>
        <h2>Products</h2>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
                <ProductCard :product="p" />
            </div>
        </div>
    </div>
</template>

<script setup>
definePageMeta({
    layout: "products",
});

// fetch products and destructure the data coming back from the API and rename it to products rather than data
const { data: products } = await useFetch("https://fakestoreapi.com/products");

useHead({
    title: "Nuxt Dojo | Merch",
    meta: [{ name: "description", content: "Nuxt 3 Merch" }],
});
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
