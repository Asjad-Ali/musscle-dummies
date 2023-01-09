<template>
  <section class="navbarPadding">

      <div class="container-fluid">
        <img class="img-fluid" style="height: 100vh" src="/f1.jpeg"/>
      </div>

      <!-- <div class="container">
        <div class="row">
          <div class="col-md-6">
            <card />
          </div>
          <div class="col-md-6">
            <card />
          </div>
        </div>
      </div> -->



      <div class="container-fluid bg-2 d-flex flex-column">
        <div class="container d-flex my-5">
          <div class="row justify-content-center">
            <div class="col-lg-4 col-md-6 col-xs-12">
              <Post title="WOMEN TOTAL WEIGHT LOSS PACKAGE" img="/women.jpeg"  desc="Includes" 
              :points="women_points"/>
            </div>
            <div class="col-lg-4 col-md-6 col-xs-12">
              <Post title="MEN TOTAL WEIGHT LOSS PACKAGE" img="/man.jpeg" desc="Includes"  :points="men_points"/>
            </div>
          </div>
        </div>
      </div>

      <div class="container-fluid text-center" style="margin-top:20px">
        <img class="img-thumbnail postWidth" src="/f2.jpeg" style="object-fit: contain;height:300px;background-color:black"/>
      </div>

      <div class="container d-flex flex-row justify-content-around" style="margin-top:20px">
        <img class="rounded" src="/football.jpeg" width="200px" height="200px"/>
        <img class="rounded" src="/logo.jpeg"  width="200px" height="200px"/>
      </div>
     
        
      <div class="container-fluid my-5 d-flex flex-row justify-content-around align-item-center text-center">
              <div class="col">
                <a href="https://www.instagram.com/muscle_dummies/" target="_blank">
                <img class="img-fluid rounded" src="/insta.jpeg" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                <a href="https://opensea.io/collection/muscle-dummies" target="_blank">
                  <img class="img-fluid rounded"  src="/opensea.png" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                  <a href="https://www.tiktok.com/@muscle_dummies?lang=en" target="_blank">
                  <img class="img-fluid rounded"  src="/tiktok.png" width="50%" height="50%"/>
                  </a>
              </div>
                <div class="col">
                <a href="https://discord.gg/faaAD7hA" target="_blank">
                  <img class="img-fluid rounded"  src="/discord.png" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                <a href="https://www.twitch.tv/muscle_dummies" target="_blank">
                  <img class="img-fluid rounded"  src="/twitch.webp" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                <a href="https://www.youtube.com/channel/UCMO1znzmHY2FO9X8T--faGw" target="_blank">
                  <img class="img-fluid rounded"  src="/youtube.png" width="50%" height="50%"/>
                </a>
              </div> 
              <div class="col">
                <a href="https://www.instagram.com/5starfbpackage/" target="_blank">
                  <img class="img-fluid rounded" src="/insta.jpeg" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                <a href="https://www.tiktok.com/@coach_isaac?lang=en" target="_blank">
                  <img class="img-fluid rounded"  src="/tiktok.png" width="50%" height="50%"/>
                </a>
              </div>
                <div class="col">
                <a href="https://5starfbpackage.com/sales-page1666127244096" target="_blank">
                    <img class="img-fluid rounded"  src="/home.png" width="50%" height="50%"/>
                </a>
              </div>
              
                <div class="col">
                <a href="https://www.twitch.tv/coach_isaac" target="_blank">
                  <img class="img-fluid rounded"  src="/twitch.webp" width="50%" height="50%"/>
                </a>
              </div>
      </div>

      <div class="container-fluid postWidth  text-center d-flex flex-column" style="text-transform: uppercase">
        <p>
          Any Question? Contact Us
        </p>
        <p>
          info@muscledummies.com
        </p>
        <p>
          © 2022, muscle dummies
        </p>
      </div>

  </section>
</template>
 
<script>
export default {
  name: 'IndexPage',
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
      .imgTopSpace{
        margin-top:50px
      }
  }
</style>