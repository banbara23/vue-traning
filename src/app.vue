<template>
  <h1 class="red">{{msg}}</h1>
</template>

<script>
    module.exports = {
        data: function() {
            return {
                msg: 'Hello world!'
            }
        }
    }
</script>

<style>
    .red {
        color: #f00;
    }
</style>