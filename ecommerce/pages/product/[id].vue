<template>
    <div>
        <section class="py-10">
            <div class="container m-auto grid lg:grid-cols-3 gap-10">
                <div class="lg:col-span-1">
                    <img :src="product.image" alt="">
                </div>
                <div class="lg:col-span-2">
                    <h1 class="text-3xl font-bold">{{ product.title }}</h1>
                    <h1 class="text-3xl">${{ product.price }}</h1>
                    <p>{{ product.description }}</p>
                    <div class="my-5 bg-warning-600 w-48 text-center rounded-full text-white py-2">{{ product.category }}</div>

                    <div class="flex gap-2 items-center">
                        <QuantitySelector />
                        <button class="bg-green-700 py-2 px-10 text-white rounded-md hover:bg-blue-900">Add to Cart</button>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
const route = useRoute()
const {data:product} = useFetch(`https://fakestoreapi.com/products/${route.params.id}`)
</script>

<style lang="scss" scoped>

</style>