<template>
    <div>
        <Head>
            <Title>Nuxt Dojo | {{ product.title }}</Title>
            <Meta name="description" :content="product.description"></Meta>
        </Head>
        <ProductDetails :product="product" />
    </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = "https://fakestoreapi.com/products/" + id;

// fetch the data

const { data: product } = await useFetch(uri, { key: id });

if (!product.value) {
    throw createError({
        statusCode: 404,
        statusMessage: "Product not found",
        fatal: true,
    });
}

definePageMeta({
    layout: "products",
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
