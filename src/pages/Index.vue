<template>
  <div class="parent">
    <!-- Introduction section -->
    <q-card class="my-card">
      <q-parallax
       src="stars.png"
       style="background:#000;height:100vh;"
      >
      <div class="twinkling"></div>
      <div style="display:flex; flex-flow:column; align-items:center;justify-content:space-between;margin-top:-10rem;">
      <h6 style="z-index:2;" :style="mobile ? 'font-size: 3rem;' : 'font-size: 8rem;'">Hello!
      </h6>
      <img width="100px" style="margin-top:2rem;z-index:2;" height="200px" src="arrow_down.gif_400" />
      </div>
      <img style="z-index:2;" :width="mobile ? '250px' : '350px' "  class="absolute-bottom-right" :height="mobile ? '350px' : '450px'" src="person1.png" />
      </q-parallax>
    </q-card>
    <!-- Developer section -->
    <div :style="mobile ? 'height:112vh;' : 'height:62vh;'" style="width:100%; text-align: center;position:relative;"  class="bg-blue-grey">
      <q-intersection
        once
        transition="scale"
      >
      <div style="padding-top:1rem;">
       <h3 :style="mobile ? 'font-size: 20px; line-height:25px;' : 'font-size: 30px;'"> Hi, my name is Muhammad. I design & build <br /> applications for several platforms.</h3>
       <div :class="mobile ? 'q-mt-lg' : ''" :style="!mobile ? 'margin-top:8rem;' : ''">
       <div class="row" style="justify-content:center;">
         <div :style="mobile ? 'padding-top:2rem;' : ''" :class="mobile ? 'col-12' : 'col-2'">
           <q-icon v-if="windows" style="position:absolute;bottom:6rem;" name="beenhere" size="sm" />
           <img width="90px"   src="windows.svg" alt="Windows 10">
          </div>
          <div :style="mobile ? 'padding-top:1rem;' : ''" :class="mobile ? 'col-12' : 'col-2'">
            <q-icon v-if="linux" style="position:absolute;" name="beenhere" size="sm" />
           <img width="100px" src="linux.svg" alt="Linux OS">
           </div>
           <div :style="mobile ? 'padding-top:1rem;' : ''" :class="mobile ? 'col-12' : 'col-2'" >
             <div>
             <q-icon style="position:absolute;" v-if="macOrios" name="beenhere" size="sm" />
             <img width="80px" src="apple.svg" alt="Mac OS & iOS">
            </div>
           </div>
           <div :style="mobile ? 'padding-top:2rem;' : ''" :class="mobile ? 'col-12' : 'col-2'">
             <q-icon v-if="android" style="position:absolute;" name="beenhere" size="sm" />
             <img width="100px" src="android.svg" alt="Android">
           </div>
       </div>
       </div>
     </div>
      </q-intersection>
      <div style="width:100%;display:flex; justify-content:center;position:absolute;bottom:0;" v-if="windows || macOrios || android || linux">
      <p class="text-caption" style=""><q-icon name="beenhere" /> Indicates your current platfrom</p>
      </div>
    </div>
    <div style="width:100%;height:.05rem;background-color:grey;"></div>
    <!-- Mobile section -->
    <div style="width:100%;position:relative; text-align: center;z-index:0;height: 77vh;"  class="bg-blue-grey-3 responsive">
         <q-intersection once transition="slide-right">
         <div v-if="mobile" class="row" style="justify-content:center;">
          <div class="col-12" style="margin-top: 2rem;">
          <h5>Building hybrid mobile applications using Apache Cordova.</h5>
          </div>
            <div class="col-12">
              <img style="position:relative;z-index:0;" width="200px" height="350px"  src="https://svgsilh.com/svg/1682317.svg" />
            </div>
          </div>
          <div v-else class="row" style="justify-content:center;">
            <div class="col-4">
              <img style="position:relative; margin-top:2rem;z-index:0;" class="responsive" width="400px" height="600px" src="https://svgsilh.com/svg/1682317.svg" />
            </div>
           <div class="col-6" style="margin-top: 10rem;">
             <h5 class="responsive" >Building hybrid mobile applications using Apache Cordova.</h5>
           </div>
       </div>
         </q-intersection>
    </div>
    <div style="width:100%;height:.05rem;background-color:grey;"></div>
    <!-- Web section -->
      <div style="width:100%;position:relative; text-align: center;z-index:0;height: 70vh;"  class="bg-blue-grey-3">
         <q-intersection once transition="slide-left">
         <div v-if="mobile" class="row" style="justify-content:center;">
          <div class="col-12" style="margin-top: 2rem;">
          <h5>Web applications using Vue js with Node js for back end.</h5>
          </div>
            <div class="col-12" style="margin-top:5rem;">
              <img style="position:relative;z-index:0;" width="150px" height="150px" src="google-chrome.svg" />
            </div>
          </div>
          <div v-else class="row" style="justify-content:center;">
           <div class="col-6" style="margin-top: 10rem;">
             <h5>Web applications using Vue js with Node js for back end.</h5>
           </div>
           <div class="col-4">
              <img class="responsive" style="position:relative; margin-top:8rem;z-index:0;" width="300px" height="300px" src="google-chrome.svg" />
            </div>
       </div>
         </q-intersection>
    </div>
    <div style="width:100%;height:.05rem;background-color:grey;"></div>
    <!-- Desktop section -->
     <div style="width:100%;position:relative; text-align: center;z-index:0;height: 70vh;"  class="bg-blue-grey-3">
         <q-intersection once transition="slide-right">
         <div v-if="mobile" class="row" style="justify-content:center;">
          <div class="col-12" style="margin-top: 2rem;">
          <h5>Hybrid desktop applications with Electron js.</h5>
          </div>
            <div class="col-12" style="margin-top:4rem;">
              <img style="position:relative;z-index:0;" width="175px" height="225px" src="monitor.svg" />
            </div>
          </div>
          <div v-else class="row" style="justify-content:center;">
            <div class="col-4">
              <img class="responsive" style="position:relative; margin-top:2rem;z-index:0;" width="400px" height="800px" src="monitor.svg" />
            </div>
           <div class="col-6" style="margin-top: 10rem;">
             <h5>Hybrid desktop applications with Electron js.</h5>
           </div>
       </div>
         </q-intersection>
    </div>
    <div style="width:100%;height:.05rem;background-color:grey;"></div>
    <!-- contact section -->
    <div :style="mobile ? 'height:710px;' : 'height:590px;'" style="position:relative;width:100%; text-align: center;z-index:1;"  class="bg-blue-grey-3">
          <div class="row" style="justify-content:center;">
          <q-intersection once class="col-12" transition="slide-left">
          <div style="margin-top:4rem;" :class="mobile ? 'col-12' : 'col-5'">
           <img :width="mobile ? '300px' : '600px'" class="responsive"  src="set.svg" alt="Windows 10">
          </div>
          <div >
          <h5>Full-stack web applications, cross-platform Mobile applications & Desktop applications.</h5>
          </div>
          </q-intersection>
       </div>
    <div style="padding-top:4rem;" :style="mobile ? 'margin-top:245px;' : 'margin-top:145px;'">
        <div class="row" style="justify-content: center;">
            <div :class="mobile? 'col-2' : 'col-1'">
                <q-btn  @click="facebook" round>
                  <q-avatar size="45px">
                    <img  src="facebook.svg">
                  </q-avatar>
                </q-btn>
            </div>
            <div :class="mobile? 'col-2' : 'col-1'">
             <q-btn @click="twitter" round>
                <q-avatar size="45px">
                  <img src="twitter.svg">
                </q-avatar>
             </q-btn>
            </div>
            <div :class="mobile? 'col-2' : 'col-1'">
             <q-btn @click="linkedin" round>
                <q-avatar size="45px">
                  <img src="linkedin.svg">
                </q-avatar>
              </q-btn>
            </div>
            <div :class="mobile? 'col-2' : 'col-1'">
              <q-btn @click="instagram" round>
                <q-avatar size="45px">
                  <img src="instagram.svg">
                </q-avatar>
              </q-btn>
            </div>
        </div>
     </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageIndex',
  data(){
    return {
      mobile : this.$q.platform.is.mobile,
      windows : this.$q.platform.is.platform === 'win',
      macOrios : this.$q.platform.is.platform === 'mac' || this.$q.platform.is.ios,
      android: this.$q.platform.is.android,
      linux: this.$q.platform.is.linux
    }
  },
  methods : {
    facebook(){
      window.open('https://www.facebook.com/muhammad.ballak.71','_blank')
    },
    twitter(){
      window.open('https://twitter.com/Muhammad3955057','_blank')
    },
    linkedin(){
      window.open('https://www.linkedin.com/in/muhammad-ballak-280b031b7','_blank')
    },
    instagram(){
      window.open('https://www.instagram.com/__muhammad1999__/','_blank')
    }
  }
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Goldman&display=swap');
div.parent{
  height: 90rem;
}
.my-card{
  border-radius: 0;
}
h6{
  color: white;
  text-shadow:0 0 0.8rem white;
  font-family: 'Goldman';
}
h3{
  color: white;
  text-shadow:0 0 0.8rem white;
  font-family: 'Noto Sans JP', sans-serif;
}
h5{
  font-family: 'Goldman';
}
.pa{
  padding-right: 1rem;;
}
/* ==============================================================================================
Nick Mkrtchyan
https://www.facebook.com/sonick.pk
http://www.Mkrtchyan.zz.mu
================================================================================================= */
* {
    margin: 0;
    padding: 0;
}
header {
    background-color:rgba(33, 33, 33, 0.9);
    color:#ffffff;
    display:block;
    font: 14px/1.3 Arial,sans-serif;
    height:50px;
    position:relative;
    z-index:5;
}
h2{
    margin-top: 30px;
    text-align: center;
}
header h2{
    font-size: 22px;
    margin: 0 auto;
    padding: 10px 0;
    width: 80%;
    text-align: center;
}
header a, a:visited {
    text-decoration:none;
    color:#fcfcfc;
}

@keyframes move-twink-back {
    from {background-position:0 0;}
    to {background-position:-10000px 5000px;}
}
@-webkit-keyframes move-twink-back {
    from {background-position:0 0;}
    to {background-position:-10000px 5000px;}
}
@-moz-keyframes move-twink-back {
    from {background-position:0 0;}
    to {background-position:-10000px 5000px;}
}
@-ms-keyframes move-twink-back {
    from {background-position:0 0;}
    to {background-position:-10000px 5000px;}
}

@keyframes move-clouds-back {
    from {background-position:0 0;}
    to {background-position:10000px 0;}
}
@-webkit-keyframes move-clouds-back {
    from {background-position:0 0;}
    to {background-position:10000px 0;}
}
@-moz-keyframes move-clouds-back {
    from {background-position:0 0;}
    to {background-position:10000px 0;}
}
@-ms-keyframes move-clouds-back {
    from {background-position: 0;}
    to {background-position:10000px 0;}
}

.stars, .twinkling, .clouds {
  position:absolute;
  top:0;
  left:0;
  right:0;
  bottom:0;
  width:100%;
  height:100%;
  display:block;
}

.stars {
  z-index:0;
}

.twinkling{
  background:url('/twinkling.png') transparent repeat top center;
  z-index:1;
  -moz-animation:move-twink-back 200s linear infinite;
  -ms-animation:move-twink-back 200s linear infinite;
  -o-animation:move-twink-back 200s linear infinite;
  -webkit-animation:move-twink-back 200s linear infinite;
  animation:move-twink-back 200s linear infinite;
}


</style>
