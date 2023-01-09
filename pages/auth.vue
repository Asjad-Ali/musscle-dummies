

<template>
 <div class="container-fluid w-100 h-100 m-0 p-0  back d-flex flex-column">
    <div class="row justify-content-center mt-5 flex-fill">
      <div class="col-lg-4 col-md-6 col-sm-6">
        <div class="card shadow" style="background-color:black;color:white">
          <div class="card-title text-center border-bottom"  >
            <h2 class="p-3">Login</h2>
          </div>
          <div class="card-body">
            <form @submit.prevent="submit">
              <div class="mb-4">
                <label for="username"  class="form-label">Email</label>
                <input type="text" class="form-control" id="username" v-model="email" />
              </div>
              <div class="mb-4">
                <label for="password"  class="form-label">Password</label>
                <input type="password" class="form-control" id="password" v-model="password"/>
              </div>

              <div class="d-flex flex-column justify-content-start">
                <div class="form-check form-check-inline">
                 <input type="radio" name="usertype" v-model="usertype" :value="0">
                  <label class="form-check-label" for="Radios1">
                    User
                  </label>
                </div>
                <div class="form-check form-check-inline">
                  <input type="radio"  name="usertype" v-model="usertype" :value="1">
                  <label class="form-check-label" for="Radios2">
                    Coach
                  </label>
                </div>
              </div>

              <div class="d-grid d-flex flex-row justify-content-center" style="margin-top:20px">
                <div v-if="loading" class="spinner-border text-danger" role="status">
                  <span class="sr-only"></span>
                </div>
                <button v-else @click="login()" type="submit" class="btn btn-primary w-50">Login</button>
              </div>
               <div class="container-fluid text-center" style="margin-top:20px">
                <a>Doesn't have an account? Signup!</a>
              </div>
            </form>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

 <script >
  import VueSimpleAlert from "vue-simple-alert";

  export default {
    data: () => ({
      usertype: "",
      password: "",
      email: "",
      loading:false
    }),
    methods: {
      async login() {
        this.loading=true;
        const user = this.$cookies.get('user') 
        var res= await fetch(
          'http://45.83.123.195:7000/api/login', {
            method: 'POST',
            headers: {
              'Accept': 'application/json',
              'Content-Type': 'application/json'
            },
            body: JSON.stringify({username: this.email, password:this.password,role:this.usertype})
          }).then(res => res.json())
        this.loading=false;
        if(res.success==1){
          this.$cookies.set('user', JSON.stringify(res), {
            path: '/',
            maxAge: 60 * 60 * 24 * 7
          })
          this.$router.replace({ name: 'index' })
        }else{
          this.$alert("Invalid email or password!");
        }
      }
    }
  }
</script>

<style scoped>
  div#__nuxt,
  #__layout,
  #__layout > div,
  #app {
    min-height: 100vh;
  }
  :root{
    --main-bg:#f56642;
  }
  .back {
    background-image: url("/backgrounds/back9.jpeg"); 
  }
  .main-bg {
    background: var(--main-bg) !important;
  }

  input:focus, button:focus {
    border: 1px solid var(--main-bg) !important;
    box-shadow: none !important;
  }

  .form-check-input:checked {
    background-color: var(--main-bg) !important;
    border-color: var(--main-bg) !important;
  }

  .card, .btn, input{
    border-radius:0 !important;
  }
  .full-height{
    width:100%;
    min-height: 100vh;
    height: 100vh;
    margin:0;
    padding:0;
    position:absolute;
    top:0px;
    right:0px;
    bottom:0px;
    left:0px;
}

</style>