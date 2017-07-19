<template>
  <div class="hello">
    <image-uploader @onChange='imgChange' :maxSize="maxSize" placeholder="+"></image-uploader>
  </div>
</template>

<script>
  import ImageUploader from '@/components/ImageUploader.vue'

  export default {
    name: 'hello',
    data () {
      return {
        maxSize: 3072 // 最大限制 单位kb
      }
    },
    components: {
      ImageUploader
    },
    methods: {
      imgChange (files) {
        if (files) {
          console.log(files)
        }
      }
    }
  }
</script>

<style scoped>

</style>
