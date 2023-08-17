<template>
    <div class="border border-neutral-200 rounded-md hover:shadow-lg w-full">
      <div class="relative">
        <SfLink href="#" class="block">
          <a :href="`/product/${product.id}`"><img
            :src="product.image"
            alt="Great product"
            class="block object-cover h-auto rounded-md aspect-square"
            width="300"
            height="300"
          /></a>
        </SfLink>
        <SfButton
          type="button"
          variant="tertiary"
          size="sm"
          square
          class="absolute bottom-0 right-0 mr-2 mb-2 bg-white ring-1 ring-inset ring-neutral-200 !rounded-full"
          aria-label="Add to wishlist"
        >
          <SfIconFavorite size="sm" />
        </SfButton>
      </div>
      <div class="p-4 border-t border-neutral-200">
        <SfLink href="#" variant="secondary" class="no-underline singleline"> {{ product.title }} </SfLink>
        <div class="flex items-center pt-1">
          <SfRating size="xs" :value="product.rating.rate" :max="5" />
  
          <SfLink href="#" variant="secondary" class="pl-1 no-underline">
            <SfCounter size="xs">123</SfCounter>
          </SfLink>
        </div>
        <p class="block py-2 font-normal leading-5 typography-text-sm text-neutral-700">
        </p>

        <span class="block pb-2 font-bold typography-text-lg">${{ product.price }}</span>
        <SfButton type="button" size="sm">
          <template #prefix>
            <SfIconShoppingCart size="sm" />
          </template>
          Add to cart
        </SfButton>
      </div>
    </div>
</template>
  
<script setup>
import { SfRating, SfCounter, SfLink, SfButton, SfIconShoppingCart, SfIconFavorite } from '@storefront-ui/vue';

defineProps({
    product:{}
})
</script>
  