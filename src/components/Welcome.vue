<template>
  <v-container class="globalContainer" fluid ma-0 pa-0>
    <v-layout row wrap>
      <v-flex xs12 sm6 class="picturesOne">
        <div class="relativeContentOne">
          <v-img max-height="1110" class="pictures" :src="picNous"></v-img>
          <div class="designTitle">
            <v-img class="designTitleImage" :src="picTitle"></v-img>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm6>
        <v-layout row wrap>
          <v-flex xs12 class="picturesTwo">
            <v-img class="pictures" :src="picVan"></v-img>
          </v-flex>
          <v-flex xs12 class="picturesThree">
            <div class="relativeContentTwo">
            <v-img class="pictures" :src="picDeco"></v-img>
              <div class="textAndButtons">
                <p class="welcomeTexte">Revivez nos beaux moments</p>
                <v-layout row wrap>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose justify-sm-center" min-width="180" href="https://www.youtube.com/playlist?list=PLdK75yPRMfO_14aidqWC-shdxeAjomYjx">Vidéo</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" min-width="180" href="https://photos.app.goo.gl/kwzip9QNdASLxzZc6">Voyage de noces</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" min-width="180" href="https://photos.app.goo.gl/fiHrnNZuEZPfPnfLA">Mariage</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" min-width="180"href="https://photos.app.goo.gl/hSxkydq3mUJ5bK4g6">Photobooth</v-btn>
                  </v-flex>
                </v-layout>
              </div>
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<style>
  .globalContainer {
    max-height: 100%;
  }

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

  .designTitleImage {
    width: 600px;
    z-index: 1;
  }

  .designTitle {
    position: absolute;
    top: 70px;
    left: -300px;
    margin-left: 50%;
  }

  .designTitleImage:before {
    content:"J";
    font-family: 'Alex Brush', cursive;
    font-size: 5.4rem;
    position: absolute;
    top: -19px;
    left: 128px;
    z-index: 3;
    color: #EED3C5;
  }
  .designTitleImage:after {
    content:"JN";
    font-family: 'Alex Brush', cursive;
    font-size: 5.4rem;
    position: absolute;
    top: -19px;
    right: 121px;
    color: #EED3C5;
  }
  
  @media screen and (min-width: 1264px) and (max-width: 1904px) {
    .designTitleImage {
      width: 500px;
    }

    .designTitle {
      top: 70px;
      left: -250px;
    }

    .designTitleImage:before {
      font-size: 4.4rem;
      top: -15px;
      left: 106px;
    }
    .designTitleImage:after {
      font-size: 4.4rem;
      top: -16px;
      right: 103px;
    }
  }

  @media screen and (min-width: 960px) and (max-width: 1263px) {
    .designTitleImage {
      width: 400px;
    }

    .designTitle {
      top: 70px;
      left: -200px;
    }

    .designTitleImage:before {
      font-size: 3.7rem;
      top: -14px;
      left: 80px;
    }
    .designTitleImage:after {
      font-size: 3.7rem;
      top: -14px;
      right: 80px;
    }
  }

  @media screen and (min-width: 600px) and (max-width: 959px) {
    .designTitleImage {
      width: 200px;
    }

    .designTitle {
      top: 70px;
      left: -100px;
    }

    .designTitleImage:before {
      font-size: 3.7rem;
      top: -14px;
      left: 80px;
    }
    .designTitleImage:after {
      font-size: 3.7rem;
      top: -14px;
      right: 80px;
    }
  }

  .welcomeTexte {
    font-family: 'Alex Brush', cursive;
    font-size: 3rem;
    text-align: center;
    color: #4A5D49;
  }

  .textAndButtons {
    position: absolute;
    bottom: 0px;
    left: 0px;
    background-color: rgba(255,255,255,0.5);
    width: 100%;
  }

  .btn-rose {
    background-color: #EED3C5 !important;
    color: #000000 !important;
    border: 3px solid #FFFFFF;
  }

  .btn-rose span {
    font-weight: 300;
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
