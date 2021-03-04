<template>
  <div v-if="jobs">
    <h1>Job Details Page</h1>
    <p>The job id {{ id }}</p>
    {{jobs.title}}
  </div>
  <div v-else>
      <h1>Loading...</h1>
  </div>
</template>

<script>
export default {
    props: ['id', 'title'],
    data(){
        return {
            jobs: null
            //id: this.$route.params.id
        }
    }
    ,
    async mounted(){
       await fetch('http://localhost:3000/jobs/'+this.id).
        then((res) => res.json())
        .then((data) => this.jobs = data)
        .catch(err => console.error(err));
    }
}
</script>

<style>

</style>