<template>
    <div class="row">
        <h1>What you want to do today?</h1>
        <input type="text" v-model='goal' class='form-control' placeholder="Delete goal by double click on it.">
        <button @click.prevent='createGoal' class='btn btn-primary'>Add Goal</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                goal: ""
            }
        },
        methods: {
            createGoal() {
                this.$emit('goalAdded', this.goal);
                this.goal = '';
            }
        }
    }
</script>

<style>
    .row {
        margin-bottom: 20px;
    }
    h1 {
        color: #fff;
        font-size: 50px;
        font-weight: bold;
    }
    button {
        margin-top: 20px;
    }
</style>

