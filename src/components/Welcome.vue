<template>
  <v-container fluid ma-0 pa-0>
    <v-layout row wrap child-flex>
      <v-flex xs12 sm6 class="picturesOne">
        <v-card height="100%-16px">
          <v-card-text>
            <div class="relativeContentOne">
              <v-img max-height="1110" class="pictures" :src="picNous"></v-img>
              <div class="designTitle">
                <v-img class="designTitleImage" :src="picTitle"></v-img>
              </div>
            </div>
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs12 sm6>
        <v-card height="100%">
          <v-card-text style="height:50%; max-width: 840px;">
            <v-img class="pictures" :src="picVan" height="100%"></v-img>
          </v-card-text>
          <v-card-text style="height:50%; max-width: 840px;">
            <div class="relativeContentTwo">
            <v-img class="pictures" :src="picDeco" height="100%"></v-img>
              <div class="textAndButtons">
                <p class="welcomeTexte">Revivez nos beaux moments</p>
                <v-layout row wrap>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose justify-sm-center" href="https://www.youtube.com/playlist?list=PLdK75yPRMfO_14aidqWC-shdxeAjomYjx">Vidéo</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" href="https://photos.app.goo.gl/kwzip9QNdASLxzZc6">Voyage de noces</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" href="https://photos.app.goo.gl/fiHrnNZuEZPfPnfLA">Mariage</v-btn>
                  </v-flex>
                  <v-flex class="text-center mb-5" xs6>
                    <v-btn class="btn-rose" href="https://photos.app.goo.gl/hSxkydq3mUJ5bK4g6">Photobooth</v-btn>
                  </v-flex>
                </v-layout>
              </div>
            </div>
          </v-card-text>
        </v-card>
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
    top: 34px;
    left: 128px;
    z-index: 3;
    color: #EED3C5;
  }
  .designTitleImage:after {
    content:"JN";
    font-family: 'Alex Brush', cursive;
    font-size: 5.4rem;
    position: absolute;
    top: 34px;
    right: 121px;
    color: #EED3C5;
  }

  .btn-rose {
    background-color: #EED3C5 !important;
    color: #000000 !important;
    border: 3px solid #FFFFFF;
    min-width: 180px !important;
  }

  .btn-rose span {
    font-weight: 300;
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
      top: 26px;
      left: 106px;
    }
    .designTitleImage:after {
      font-size: 4.4rem;
      top: 26px;
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
      font-size: 3.5rem;
      top: 19px;
      left: 85px;
    }
    .designTitleImage:after {
      font-size: 3.5rem;
      top: 19px;
      right: 80px;
    }
  }

  @media screen and (min-width: 600px) and (max-width: 959px) {
    .designTitleImage {
      width: 250px;
    }

    .designTitle {
      top: 70px;
      left: -125px;
    }

    .designTitleImage:before {
      font-size: 2.2rem;
      top: 7px;
      left: 52px;
    }
    .designTitleImage:after {
      font-size: 2.2rem;
      top: 7px;
      right: 51px;
    }

    .btn-rose {
      border: 3px solid #FFFFFF;
      min-width: 127px !important;
    }

    .btn-rose span {
      font-weight: 300;
      font-size: 0.5rem;
    }
  }

  @media screen and (max-width: 599px) {
    .designTitleImage {
      width: 300px;
    }

    .designTitle {
      top: 70px;
      left: -150px;
    }

    .designTitleImage:before {
      font-size: 2.7rem;
      top: 11px;
      left: 63px;
    }
    .designTitleImage:after {
      font-size: 2.7rem;
      top: 11px;
      right: 60px;
    }
  }

  .welcomeTexte {
    font-family: 'Alex Brush', cursive;
    font-size: 3rem;
    text-align: center;
    color: #4A5D49;
    margin-bottom: 25px;
  }

  .textAndButtons {
    position: absolute;
    bottom: 0px;
    left: 0px;
    background-color: rgba(255,255,255,0.5);
    width: 100%;
    height: 200px;
    padding-top: 25px;
  }

  .v-card {
    box-shadow: none;
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
