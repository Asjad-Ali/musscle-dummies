<template>
  <div class="container-fluid p-0 d-flex flex-column">
  <section class="navbarPadding">
      <div class="container-fluid bg-2 d-flex flex-column">

        <div class="container postWidth">
            <div class="row">
              <div class="col-lg-6 col-md-6 col-xs-12">
                <Post title="WOMEN TOTAL WEIGHT LOSS PACKAGE" img="/women.jpeg"  desc="Includes" 
                :points="women_points" h="400px"/>
              </div>

              <div class="col-lg-6 col-md-6 col-xs-12">
                <Post title="MEN TOTAL WEIGHT LOSS PACKAGE" img="/man.jpeg" desc="Includes"  :points="men_points"/>
              </div>

            </div>
        </div> 
          
        <div class="container postWidth" style="padding-top:2%">
            <div class="row">
              <div class="col-lg-4 col-md-4 col-xs-12">

              <NuxtLink to="/fivestar" style="text-decoration: none;">
                <Post title="5 STAR FOOTBALL PACKAGE"  img="/football.jpeg"
                  desc="The BEST product for HSFB Players - Everything you need for success!"
                  more="This package includes."
                  v-bind:points="star_points"
                />
              </NuxtLink> 
               

              </div>

              <div class="col-lg-4 col-md-4 col-xs-12">
                <Post title="nutrition Guides"  img="/m1.jpeg" desc="Includes" :points="meal_points" />
              </div>
              <div class="col-lg-4 col-md-4 col-xs-12">
                <Post  title="WORKOUT PLANS" img="/m2.jpeg"  desc="Includes" :points="work_points"/>
              </div>
             
            </div>
        </div>   <!----------------- Post  end-------------------->
         <div class="container postWidth" style="padding-top:2%">
            <div class="row">
              <div class="col-lg-4 col-md-4 col-xs-12">
               <Post title="MUSCLE DUMMIES COOKBOOK PACKAGE" img="/m3.jpeg" desc="coming soon" recommend="true" />
              </div>
            </div>
        </div><br/><br/>
        <div class="flex-fill"></div>

           <!----------------- Footer  start-------------------->
        <!-- <div class="container footer d-flex flex-row justify-content-start p-0">

          <img class="img-fluid" src="/football.jpeg" style="height:200px;object-fit: fill; width=300px"/>
          <div class="d-flex flex-grow-5 w-100">
            <img class="img-fluid w-100" src="/f1.jpeg" style="height:200px;object-fit: fill; width=300px"/>
          </div>
       </div> --------------- Footer  end------------------ -->
          

    </div> 

  </section>
  </div>
</template>
 
<script>
export default {
  name: 'ShopPage',
  target: 'static',
  data () {
    return {
      star_points:[
        'Winter D1 FB Workout Plan',
        'Winter D1 FB Speed & Conditioning Plan',
        'Off Season FB Nutrition Guide',
        'HSFB Recruiting Templates',
        'Twitter Profile Setup',
        'Winter Sports and Non Sports Schedule',
        'Injury/Mobility Exclusive Content'
      ],
      women_points:[
        '4-week at home beginner workout',
        '8-week beginner workout',
        "Women's weight loss nutrition guide"
      ],
      men_points:[
        '4-week at home beginner workout',
        '8-week beginner workout',
        "Men's weight loss nutrition guide"
      ],
      meal_points:[
        "Women's muscle gain nutrition guide",
        "Men's muscle gain nutrition guide"
      ],
      work_points:[
        "4-week at home beginner workout",
        "8 week beginner workout",
        "10 week bulk workout",
        "10 week muscle gain",
        "10 week shred program"
      ]
    }
  },

  head () {
    return {
      title: 'Test Page - My awesome project',
      link: [
        { rel: 'stylesheet', href: '~/node_modules/bootstrap/dist/css/bootstrap.min.css' }
      ],
      script: [
        { src: "~/node_modules/bootstrap/dist/js/bootstrap.bundle.min.js", type: "text/javascript"}
      ]

    }
  }, 
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
  }
</style>