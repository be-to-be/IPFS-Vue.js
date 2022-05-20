<template>
  <div>

    <div class=" d-flex align-items-center justify-content-center" style ="height: 520px; padding-top: 40px; margin-top:40px;">
      <div class="row justify-content-center">
        <div class="col-md-7 align-middle" style="padding-top: 15%;">
          <p style="font-size: 40px; font-weight:bold; width: 100%;">IPFS Blog Engine | Render Machine</p>
          <input v-model = "rootCID" type="text" placeholder="Drop your blog's URI here..."  class="form-control border border-dark border-2 d-inline" style="width: 70%;">
          <button @click="renderCID" class="btn btn-outline-dark border border-dark border-2 ms-4">Render it!</button>
          <p class=" mt-3" style="font-size: 20px;" >Haven't created blog yet? <span><router-link to="/" style="color: black;">Click here</router-link></span></p>




        </div>
        <div class="col-md-5">
          <!-- afefefe -->
          <img style = "width: 100%; height: 100%" src="../../assets/doodle-machine-2.png">
        </div>

      </div>

      </div>
    <Footer/>
  </div>


      <!-- <div class="row">
        <div class="col-md-8">
          <div class="text-center">
            <h3>IPFS Blog Engine | Render Machine</h3>
          </div>
          <div class="row">
            <div class="col-md-8">
              <input v-model = "rootCID" type="text" class="form-control border border-dark border-2" placeholder="Drop your blog's URI here..." >
            </div>
            <div class="col-md-4">
                <button @click="renderCID" class="btn btn-outline-dark">Render it!</button>
            </div>
          </div>
          <p class="text-center" >Haven't created blog yet? <span><router-link to="/">Click here</router-link></span></p>
    
        </div>
        <div class="col-md-4">
          <img style = "width: 100%; height: 100%" src="../../assets/doodle-machine-2.png">
        </div>
      </div> -->

      <!-- <div class="bg-warning">sgsfgsrg</div> -->
    <!-- </div> -->
  <!-- <div class="d-flex align-items-center justify-content-center" style="height: 100%;">
      <div class="row">
        <div class="col-md-8">
          <div class="d-flex align-items-center justify-content-center">
            <h3>IPFS Blog Engine | Render Machine</h3>
          </div>
          <div class="row">
            <div class="col-md-8">
              <input v-model = "rootCID" type="text" class="form-control" placeholder="Drop your blog's URI here..." >
            </div>
            <div class="col-md-4">
                <button @click="renderCID" class="btn btn-outline-dark">Render it!</button>
            </div>
          </div>
          <p class="text-center" >Haven't created blog yet? <span><router-link to="/create-blog">Click here</router-link></span></p>
    
        </div>
        <div class="col-md-4">
          <img style = "width: 100%; height: 100%" src="../../assets/doodle-machine-2.png">
        </div>
      </div>
  </div> -->
</template>

<script>
import Footer from '../../components/Footer/index.vue'
export default {
  name: "RenderMachine",
  components: {Footer},

    data() {
    return {
      rootCID: ''
    };
  },
  methods: {
    renderCID(){
    //   this.$router.push('/create-blog')
      if(this.rootCID != ''){
        this.$router.push(`/blog/${this.rootCID}`)
      }

    },
  }
}
</script>

<style lang="scss">

</style>

<style scoped>

</style>
