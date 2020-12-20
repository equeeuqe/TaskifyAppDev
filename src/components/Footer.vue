<template>
  <footer>
      <p>Copyright 2020 {{ title }} </p>
  </footer>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true
        }
    },
    data() {
        return{

        }
    }
}
</script>

<style scoped>
    footer{
        background: #fad744;
        padding: 6px;
    }
    
    p{
        color: #2b3252;
        text-align: center;
    }
</style>