<script>
export default {
  name: "ProjectCard",
  props:{
    projectList: Array,
    technologyList: Array,
    typeList: Array
    },
  data(){
    return {
      
      }
  }
}
</script>
<template>
  <div 
  v-for="project in projectList" :key="project.id"
  class="card me-4 mb-4" style="width: 18rem;">
  <img class="card-img-top" :src="project.cover_image" :alt="project.name">
  <div class="card-body">
    <h5 class="card-title">{{project.name}}</h5>

    <div class="text-danger">
    <span v-for="type in typeList" :key="type.id">
      {{type.id == project.type_id ? type.name : ''}}
      </span>
    </div>
    <div class="bg-dark">
      <span class="text-white">Technologies here</span>
    </div>
    <p class="card-text">{{project.summary}}</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
</template>


<style>

</style>