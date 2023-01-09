<!-- Please remove this file from your project -->
<template>
  <div class="card  p-0 cardMargin" style="color:black; text-transform: uppercase;">

    <div class="card-header justify-content-center">
     <h6 class="mx-auto text-center oneline" >{{title}}</h6>
    </div>

    <div class="card-body p-0 m-0" style="background-color:black">
      <img class='img-fluid align-self-center' v-bind:src="img" style="width:100%;object-fit:fill;height:400px"/>
    </div>

    <div class="card-footer">

      <p class="m-0 p-0 align-self-center " style="font-size:14px;padding-left:5px">{{desc?desc:''}}</p>
      
      <p class="m-0 align-self-center p-0 " style="font-size:12px;padding-left:5px">{{more?more:''}}</p>
    
      <div v-if="points" style="font-size:12px" class="container-fluid d-flex flex-column align-items-start">
        <li v-for="pt in points" :key="pt">{{pt}}</li>
      </div>
      <div v-if="recommend" class="container-fluid text-center pt-5">
        <div  class="btn btn-primary" >Make a Recommend</div>
      </div>

    </div>

  </div>
</template>

<script>
  export default {
    target: 'static',
    name: 'HomePost',
    props:['title','img','desc','more','points','recommend']
  }
</script>

<style scoped>
 .oneline{
   overflow: hidden;
   text-overflow: ellipsis;  
  text-align: center;
   display: -webkit-box;
   -webkit-line-clamp: 3; /* number of lines to show */
           line-clamp: 3; 
   -webkit-box-orient: vertical;
  } 
  @media all and (min-width: 480px) {
    .cardMargin{
      margin-top:0px;
    }
  }

  @media all and (max-width: 479px) {
    .cardMargin{
      margin-top:40px;
    }
  }
</style>