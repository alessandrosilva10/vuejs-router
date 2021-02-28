<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{name: 'JobDetails', params: {id: job.id}}">
          <h2>{{ job.title }}</h2>
      </router-link>
  </div>
</template>
404 pages and redirects
<script>
export default {
    data: () => ({
        jobs: [
            { id: 1, title: 'Ninja UX Designer', details: 'UX Designer' },
            { id: 2, title: 'Ninja Web Designer', details: 'Web Designer' },
            { id: 3, title: 'Ninja Vue Designer', details: 'Vue Designer'},
        ]
    })
}
</script>

<style>
    .job a {
        text-decoration: none;
    }
    .job h2{
        background: #f4f4f4;
        padding: 20px;
        border-radius: 10px;
        margin: 10px auto;
    }
    .job h2:hover {
        background: #ddd;
    }
</style>