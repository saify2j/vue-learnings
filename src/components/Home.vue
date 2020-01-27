<template>

    <div>
        <link href="https://fonts.googleapis.com/css?family=Ubuntu&display=swap" rel="stylesheet">
        <h1>{{ msg }}</h1>

    </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'We have achieved social media'
    }
  }
}
</script>
<style scoped>
    h1{
        font-family: 'Ubuntu';

    }
</style>
