<template>
  <v-container fluid ma-0 pa-0>
    <v-layout row wrap>
      <v-flex xs6 class="picturesOne">
        <div class="relativeContentOne">
          <v-img class="pictures" :src="picNous"></v-img>
          <div class="designTitle">
            <v-img class="designTitleImage" :src="picTitle"></v-img>
          </div>
        </div>
      </v-flex>
      <v-flex xs6>
        <v-layout row wrap>
          <v-flex xs12 class="picturesTwo">
            <v-img class="pictures" :src="picVan"></v-img>
          </v-flex>
          <v-flex xs12 class="picturesThree">
            <div class="relativeContentTwo">
            <v-img class="pictures" :src="picDeco"></v-img>
              <div class="textAndButtons">
                <p class="welcomeTexte">Revivez nous beaux moments</p>
                <v-btn>Vidéo</v-btn>
                <v-btn>Galerie</v-btn>
              </div>
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<style>
  .pictures {
    border-radius: 1.5rem;
  }

  .relativeContentOne{
    position: relative;
    width: 100%;
    height: 100%;
  }

  .relativeContentTwo {
    position: relative;
    width: 100%;
    height: 100%;
  }

  .picturesOne {
    padding-top: 1.5rem;
    padding-bottom: 3rem;
    padding-left: 3rem;
    padding-right: 1.5rem;
  }
  .picturesTwo {
    padding-top: 1.5rem;
    padding-bottom: 1.5rem;
    padding-left: 1.5rem;
    padding-right: 3rem
  }
  .picturesThree {
    padding-top: 1.5rem;
    padding-bottom: 3rem;
    padding-left: 1.5rem;
    padding-right: 3rem;
  }

  .designTitle {
    position: absolute;
    top: 70px;
    left: -200px;
    margin-left: 50%;
  }

  .designTitleImage {
    width: 400px;
    z-index: 1;
  }

  .designTitleImage:before {
    content:"J";
    font-family: 'Alex Brush', cursive;
    font-size: 3.7rem;
    position: absolute;
    top: -14px;
    left: 80px;
    z-index: 3;
    color: #EED3C5;
  }
  .designTitleImage:after {
    content:"JN";
    font-family: 'Alex Brush', cursive;
    font-size: 3.7rem;
    position: absolute;
    top: -14px;
    right: 80px;
    color: #EED3C5;
  }

  .welcomeTexte {
    font-family: 'Alex Brush', cursive;
    font-size: 3rem;
    text-align: center;
    color: #4A5D49;
  }

  .textAndButtons {
    position: absolute;
    top: 50px;
    left: 0px;
    background-color: rgba(255,255,255,0.5);
    width: 100%;
  }
</style>

<script>
export default {
  data: () => ({
    picVan: require('./../assets/Van.jpg'),
    picNous: require('./../assets/Nous.jpg'),
    picDeco: require('./../assets/Deco.jpg'),
    picTitle: require('./../assets/titleHeart.svg')
  })
};
</script>
