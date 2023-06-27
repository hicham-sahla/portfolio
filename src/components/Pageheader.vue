<template>
  <div id="pageheader" class="text-center py-5" style="margin-top: 100px;">
    <h1 class="display-4 mb-1 text-primary" style="font-weight: 600;">Hi! I am Hicham</h1>
    <h2 class="display-6 mb-5 text-primary">A passionate webdeveloper</h2>
    <div class="d-flex justify-content-center">
      <div class="rounded-circle overflow-hidden" style="width: 200px; height: 200px;">
        <img :src="require('@/assets/hicham.jpg')" class="img-fluid" alt="Hicham Sahla">
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'PageheaderSection',
  data() {
    return {
      skills: ['JavaScript', 'Vue.js', 'React', 'Node.js']
    }
  }
}
</script>
