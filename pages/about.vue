<template>
    <main>
        <h1>Dad Jokes</h1>
        <p>List corny dad jokes just for you :)</p>
        <NuxtLink to="/">Go To Homepage</NuxtLink>
    </main>
</template>
<script>
    export default {
        head() {
            return {
                title: 'Dad Jokes | About',
                meta: [
                    {
                        hid: 'description',
                        name: 'description',
                        content: 'Corny Dad Jokes make you fun!'
                    }
                ]
            }
        }
    }
</script>