<template>
  <div class="home">
    <h3>List Projects</h3>
    <div id="projects">
      <div class="project" v-for="(project, index) in getProject" :key="index">
        <router-link :to="{ name: 'DetailProject', params: { id: project.id } }">
          <button>{{project.name}}</button>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  components: {},
};
</script>

<style scoped>
  button{
    border: none;
    width: 400px;
    height: 50px;
    margin-bottom: 1%;
    background: #80A1FF;
    border-radius: 8px;
    color: white;
    transition: all 0.5s;
  }

  button:hover{
    background: #2b5fec;
  }
</style>
