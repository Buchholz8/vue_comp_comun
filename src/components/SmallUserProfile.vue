<template>
    <div>
       <h3> {{user[`name`]}} </h3>
       <p> {{user[`age`]}} </p>
       <h5 v-if="user[`is_premium`] === true"> Premium</h5>
       <p v-else> basic</p>
       <button @click="user_clicked"> Click Me</button>
    </div>
</template>

<script>
    export default {
        methods: {
            user_clicked( ) {
                this.$emit(`user_clciked` , this.user[`name`])
            },
        },
        props: {
            user: Object,
        }
    }
</script>

<style scoped>

</style>