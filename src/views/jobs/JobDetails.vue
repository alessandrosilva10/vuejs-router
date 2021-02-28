<template>
  <h1>Job Details Page</h1>
  <p>The job id {{ id }}</p>
  {{title}}
</template>

<script>
export default {
    props: ['id', 'title'],
    data(){
        return {
            //id: this.$route.params.id
        }
    }
}
</script>

<style>

</style>