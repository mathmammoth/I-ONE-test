<template>
    <section class="p-10">
        

        <ul>
            <li class="font-semibold pt-2" v-for="user of users" :key="user">
            <a href="#" @click.prevent="openUser(user)">{{user.name}} </a>
            </li>
        </ul>
    </section>
</template>


<script>
export default {
    async fetch({store}) {
        if(store.getters['users/users'].length === 0) {
            await store.dispatch('users/fetch')
        }
    },
    data: () => ({
        pageTitle: 'Users page'
    }),

    computed: {
        users() {
            return this.$store.getters['users/users']
        }
    },

methods: {
    openUser(user) {
        this.$router.push('/users/' + user.id)
    }
}
}
</script>