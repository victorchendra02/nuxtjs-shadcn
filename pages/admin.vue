<script setup>
definePageMeta({
    layout: "default",
});
</script>

<template>
    <div>
        <h1 class="text-4xl font-bold">admin.vue</h1>
        <br />

        <Button class="cursor-pointer" variant="outline" @click="count++">Click me</Button>
        <p>{{ count }}</p>
    </div>
</template>

<script>
export default {
    data: () => ({
        count: 0,
    }),
};
</script>
