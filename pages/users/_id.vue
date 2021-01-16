<template>
    <section class="pl-10">
        <h1 class="font-bold">{{user.name}}</h1>

        <hr>

        <h3>{{user.email}}</h3>
    </section>
</template>

<script>
export default {
    validate({params}) {
        
        return /^\d+$/.test(params.id)
    },

    async asyncData({$axios, params}) {
        const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
        return {user}
    },

}
</script>