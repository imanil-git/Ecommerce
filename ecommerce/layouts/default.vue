<template>
    <div>
        <header>
            <Navbar />
        </header>
        <main>
            <slot></slot>
        </main>
        <footer></footer>
    </div>
</template>

<script setup>

</script>

<style>
.singleline{
    display: block;
    text-overflow: ellipsis;
    line-clamp: 1;
    overflow: hidden;
    white-space: nowrap;
}
</style>