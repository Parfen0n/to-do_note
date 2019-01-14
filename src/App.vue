<template>
    <div class="container">
        <app-new-goal @goalAdded='newGoal'></app-new-goal>
        <app-goal-grid :goals='goals' @goalDeleted='deleteGoal'></app-goal-grid>
    </div>
</template>

<script>
    import NewGoal from './components/NewGoal';
    import GoalGrid from './components/GoalGrid';

    export default {
        data() {
            return {
                goals: [
                    'Something intresting'
                ]
            }
        },
        methods: {
            newGoal(goal) {
                this.goals.push(goal);
            },
            deleteGoal(index) {
                this.goals.splice(index, 1);
            }
        },
        components: {
            appNewGoal: NewGoal,
            appGoalGrid: GoalGrid
        }
    }
</script>

<style>
    body {
        background-color: #36CDFF;
        margin-top: 180px;
    }
</style>
