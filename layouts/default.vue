<template>
    <main class="vh-100 bg-light">
        <dad-nav :title="'Dad Jokes'" class="mb-4" />
        <Nuxt />
    </main>
</template>
<script>
    import DadNav from '@/components/layout/Navbar.vue'
    export default {
        components: {
            DadNav
        }
    }
</script>