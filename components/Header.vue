<template>
    <div class="container-fluid p-0 d-flex flex-column">        
        <nav class="navbar navbar-expand-sm bg-light navbar-light fixed-top m-0 p-0 d-flex flex-column" >
            <div style="background-color:bisque" class="container-fluid  w-100 deskContent">
                <div  class="container-fluid d-flex flex-column justify-content-center align-items-center">
                    <h3 class="text-center text-uppercase mb-1 fs-5">
                        Welcome to muscle DUMMIES
                    </h3> 
                </div>
            </div>
    
            <div class="container-fluid" style="background-color:white">
                <div class="d-flex flex-row align-items-center">
                    <button class="navbar-toggler mt-3" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavbar"><span class="navbar-toggler-icon"></span></button>
                    <h6 class="text-center align-self-center phoneContent" style="text-transform: uppercase;margin-top:20px;margin-left:20px">
                    Welcome to muscle DUMMIES
                    </h6> 
                </div>
            
                <div class="collapse navbar-collapse" id="collapsibleNavbar">
                <ul class="navbar-nav align-items-center w-100 justify-content-center">
                    <a class="navbar-brand phoneContent" style="margin-left:10px" href="#"><img src="https://www.muscledummies.com/static/e151eb55c8fd67573606c9fcc06394d0/299bc/icon.webp" /></a>
                    <li class="nav-item h5">
                    <a class="nav-link" href="#">Coaching</a>
                    </li>
                    <li class="nav-item h5">
                    <nuxt-link to="/shop" class="nav-link" href="#">Shop</nuxt-link>
                    </li>
                    <li class="nav-item h5">
                    <a class="nav-link" href="#">NFT</a>
                    </li>
                    <li>
                    <nuxt-link to="/" class="navbar-brand deskContent" style="margin-left:10px" href="#"><img src="https://www.muscledummies.com/static/e151eb55c8fd67573606c9fcc06394d0/299bc/icon.webp" /></nuxt-link>
                    </li>
                    <li class="nav-item h5">
                        <a class="nav-link" href="#">About</a>
                    </li>
                    <li class="nav-item h5">
                        <a class="nav-link" href="#">The App</a>
                    </li>
                    <li class="nav-item h5">
                        <a class="nav-link" href="#">My Plans</a>
                    </li>  
                    <li class="nav-item phoneContent h5">
                        <a class="nav-link" href="#">Login</a>
                    </li>  
                    <li class="nav-item deskContent h5">
                      <div class="col-1">
                        <nuxt-link to="/profile" class="nav-link" >
                                <img src="https://www.clipartmax.com/png/middle/97-978328_avatar-icon-free-fa-user-circle-o.png" width="25px" height="25px"/>
                        </nuxt-link> 
                      </div>
                    </li>
  
                </ul>
                </div> 
                <div class="d-flex flex-row">
                  <div class="nav-item h5 me-2">
                    <nuxt-link to="/login"><button class="btn btn-primary btn-md">Login</button></nuxt-link>
                  </div>    
                  <div class="nav-item h5">
                    <nuxt-link to="/signup"><button class="btn btn-primary btn-md">Signup</button></nuxt-link>
                  </div>  
              </div>
            </div>
      </nav> 
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  .line{
    display: block;
    height: 2px; 
    margin-bottom: 0px;
    background-color: rgb(0, 0, 0);
    margin-left: 20px;
    margin-right: 20px;
  }
  .line1{
    display: block;
    height: 2px; 
    margin-bottom: 0px;
    background-color: rgb(0, 0, 0);
    margin-left: 40px;
    margin-right: 40px;
  }  
  .fill { 
    min-height: 100vh;
    height: 100%;
    min-width: 100%;
  }
  .bg-2 {
    background-color: #fff;
  }
  li{
    margin-left:3%;
  }
  @media all and (min-width: 480px) {
    .deskContent {display:block;}
    .phoneContent {display:none;}
    .postWidth{
      width:70%
    }
    .navbarPadding{
     padding-top:10%;
    }
    .footer{
      width: 70%; 
      height:100px; 
    }
  }

  @media all and (max-width: 479px) {
      .deskContent {display:none;}
      .phoneContent {display:block;}
      .postWidth{
        width:95%
      }
      .navbarPadding{
        padding-top:25%;
      }
      .imgTopSpace{
        margin-top:50px
      }
  }
</style>