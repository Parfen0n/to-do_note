<template>
    <div class="row justify-content-center">
        <app-goal v-for='(goal, index) in goals' :key="goal.id" @dblclick.native='deleteGoal'>
            {{ index + 1}}. {{ goal }} 
        </app-goal>
    </div>
</template>

<script>
    import Goal from './Goal.vue';

    export default {
        props: ['goals'],
        components: {
            appGoal: Goal
        },
        methods: {
            deleteGoal(index) {
                this.$emit('goalDeleted', index);
            }
        }
    }
</script>

<style scoped>

</style>

