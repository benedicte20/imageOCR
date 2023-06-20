<script >


export default {
  data(){
    return {
      image: null
    }
  },
  computed: {
    filename(){
      return this.image ? this.image.name : 'filename';
    }
  },
  methods:{
    uploadFile: function (event){
      let files = event.target.files;
      this.image = files[0];
    },
    sendFile: function (){
      console.log(image);
    }
  }
}
</script>

<template>
 <div id='container'>
  <div class="imageUploader">
 
  <div class="file has-name is-fullwidth">
  <label class="file-label">
    <input class="file-input" type="file" name="resume" @change="uploadFile($event)">
    <span class="file-cta">
      <span class="file-icon">
        <i class="fas fa-upload"></i>
      </span>
      <span class="file-label">
        Choose a file…
      </span>
    </span>
    <span class="file-name">
      {{filename}}
    </span>
  </label>
  <button class="button ml-2">Send</button>
</div>
    

  </div>
 
 </div>
</template>

<style scoped>
.imageUploader{
 margin-top: 2rem;
}

/* .m-2{
  margin-left: 1rem ;
} */

</style>
