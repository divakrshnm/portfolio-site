<template>
  <div>
    <div class="home text-xs-center" id="home">
      <v-container fluid class="ma-0 pa-0">
        <v-parallax height="700" dark src="background.jpg">
          <v-layout align-center column justify-center class="mt-5">
            <p class="font-weight-thin mt-2" style="font-size:50px;">Selamat datang di..</p>
            <p class="font-weight-light mb-3" style="font-size:50px;">divakrishnam</p>
            <v-btn href="#portfolio" depressed medium color="white--text " class="mb-0" fab dark>
              <v-icon dark>arrow_downward</v-icon>
            </v-btn>
          </v-layout>
        </v-parallax>
      </v-container>
    </div>

    <div id="portfolio">
      <v-layout row wrap class="home text-xs-center mt-5">
        <v-flex xs12 sm12 lg12 class="mt-3">
          <p class="font-weight-light mt-5" style="font-size:40px;">Proyek Saya</p>
          <v-divider class="mb-5"></v-divider>
        </v-flex>
      </v-layout>
      <v-layout row wrap align-center justify-center>
        <v-flex xs12 sm12 lg12>
          <p class="font-weight-thin mt-2 ml-4 mt-5" style="font-size:35px;">Android Development</p>
        </v-flex>
        <v-flex xs12 sm6 md4 lg3 ma-5 v-for="android in androidCards" :key="android.name">
          <v-hover>
            <v-card slot-scope="{hover}" :class="`elevation-${hover ? 8 : 2}`" max-width="400">
              <v-card-media :src="android.img" height="200px"></v-card-media>
              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">{{android.heading}}</h3>
                  <div>{{android.content}}</div>
                </div>
              </v-card-title>

              <v-card-actions>
                <v-layout align-end column justify-end>
                  <v-btn flat color="black" :href="android.link">Lihat</v-btn>
                </v-layout>
              </v-card-actions>
            </v-card>
          </v-hover>
        </v-flex>
      </v-layout>

      <v-layout row wrap align-center justify-center>
        <v-flex xs12 sm12 lg12>
          <p class="font-weight-thin mt-2 ml-4" style="font-size:35px;">AR Development</p>
        </v-flex>
        <v-flex xs12 sm6 md4 lg3 ma-5 v-for="ar in arCards" :key="ar.heading">
          <v-hover>
            <v-card slot-scope="{hover}" :class="`elevation-${hover ? 8 : 2}`" max-width="400">
              <v-card-media :src="ar.img" height="200px" fluid-grow></v-card-media>
              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">{{ar.heading}}</h3>
                  <div>{{ar.content}}</div>
                </div>
              </v-card-title>

              <v-card-actions>
                <v-layout align-end column justify-end>
                  <v-btn flat color="black" :href="ar.link">Lihat</v-btn>
                </v-layout>
              </v-card-actions>
            </v-card>
          </v-hover>
        </v-flex>
      </v-layout>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      androidCards: [
        {
          heading: "Wind",
          content:
            "Wind menghubungkan Anda dengan penulis lain dari berbagai dunia.",
          link:
            "https://play.google.com/store/apps/details?id=com.kxland.divakrishnawind",
          img:
            "https://lh3.googleusercontent.com/p-l6wYXOKuXgZ85etsG1djPsTvJkoGZhBtanF8mqU-P_4j2W2Y3vKCY5RZLtCtaT5aKd=w1366-h626"
        }
      ],
      arCards: [
        {
          heading: "AR Gudang FG",
          content: "AR Gudang FG mengenalkan produk-produk sehari-hari.",
          link:
            "https://play.google.com/store/apps/details?id=com.kxland.argudangfg",
          img:
            "https://lh3.googleusercontent.com/vNdTT0JHZgG8Mc8UcqLh8jLdVWTaqmFdAH-vrAXKTQHnU3qKtF9xkeqEVe3PV5_36Q=w1366-h626"
        },
        {
          heading: "Edu Warehouse",
          content: "Edu Warehouse mengenalkan prosedur di dunia logistik.",
          link:
            "https://play.google.com/store/apps/details?id=com.kxland.eduwarehouse",
          img:
            "https://lh3.googleusercontent.com/koWoB8e2wDm_adeHAL72XcLwkUXu15r4uP61tx1m7dt4lIYlGoe0SBEPuc-iGDCaAog=w1366-h626"
        }
      ]
    };
  }
};
</script>

