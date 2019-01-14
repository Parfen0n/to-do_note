<template>
        <div class="col-12 alert alert-info">
            <slot></slot>
        </div>
</template>

<script>
    export default {

    }
</script>


<style>
    .alert {
        color: #3BA2FF;
        font-size: 18px;
        font-weight: bolder;
    }
    .alert-info {
        background-color: #fff;
    }
</style>

