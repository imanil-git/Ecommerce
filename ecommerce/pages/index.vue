<template>
    <div>
        <!-- Hero Section -->
        <Hero />
        <!-- Product Section -->
        <section class="py-10">
            <div class="container m-auto grid lg:grid-cols-4 md:grid-cols-3 gap-5">
                <div v-for="(product, index) in products" :key="index">
                    <ProductCard :product="product" />
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style lang="scss" scoped>

</style>