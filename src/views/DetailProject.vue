<template>
  <div id="detail">
    <article v-if="projectById !== undefined">
      <h1>{{projectById.name}}</h1>
      <p class="description">{{projectById.description}}</p>
      <hr>
      <img id="img" :src="projectById.image">
    </article>
    <article v-else>
      <h1>Project Not Found</h1>
    </article>
  </div>
</template>

<script>
export default {
  name: 'DetailProject',
  computed: {
    projectById() {
      return this.getProject.find((project) => project.id === this.$route.params.id);
    },
  },
};
</script>

<style scoped>
  .description{
    margin: 0;
    margin: auto;
    width: 50%;
    text-align: center;
  }

  #img{
    margin-top: 3%;
    width: 80%;
  }
</style>
