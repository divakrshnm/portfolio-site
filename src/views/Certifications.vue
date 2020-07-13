<template>
  <div>
    <div id="portfolio" class="mt-4">
      <v-layout row wrap class="home text-xs-center">
        <v-flex xs12 sm12 lg12>
          <p class="font-weight-light mt-5" style="font-size:35px;">Sertifikat</p>
          <v-divider></v-divider>
        </v-flex>
      </v-layout>
    </div>

    <v-container>
      <v-timeline dense>
        <v-timeline-item
          v-for="certificate in certificates"
          v-bind:color="certificate.color"
          :key="certificate.heading"
          small
        >
          <v-card light>
            <v-card-title class="title">
              <p class="font-weight-light" style="font-size:24px;">{{certificate.heading}}</p>
            </v-card-title>
            <v-card-text class="white text--primary" style="font-size:20px;">
              <p class="font-weight-thin">{{certificate.content}}</p>
              <v-btn round small outline color="green" v-bind:href="certificate.link" depressed fab>
                <v-icon color="success">arrow_forward</v-icon>
              </v-btn>
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      certificates: [
        {
          heading: "Memulai Pemrograman Dengan Python",
          color: "purple lighten-2",
          content: "Sertifikat kelulusan dari Dicoding.",
          link:
            "https://drive.google.com/file/d/1NrBvxOX2cLdZ4KVocelDIryJM9niR9W7/view?usp=sharing"
        },
        {
          heading: "Belajar Dasar Visualisasi Data",
          color: "black lighten-1",
          content: "Sertifikat kelulusan dari Dicoding.",
          link:
            "https://drive.google.com/file/d/1ELtK8a5LP-9hhCJMDX-8upPKd1s6TTVd/view?usp=sharing"
        },
        {
          heading: "Belajar Machine Learning Untuk Pemula",
          color: "cyan lighten-1",
          content: "Sertifikat kelulusan dari Dicoding.",
          link:
            "https://drive.google.com/file/d/1KQ41i1pnx5BNfwAvOmWvb2AQF3kygXoC/view?usp=sharing"
        },

        {
          heading: "Data Wrangling Python",
          color: "red lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1JlKa3Qg-0J62D6gzZpKFrOeI0gpW9Dxf/view?usp=sharing"
        },
        {
          heading: "Basic Feature Discovering for Machine Learning",
          color: "green lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/17DTJj0y9ztu9-p9WpshVBYegILZEi6r6/view?usp=sharing"
        },
        {
          heading: "Python for Data Professional Beginner - Part 1",
          color: "orange lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1d2y6R2ABgGAP_XN-ImSWcd_GPKYhlTz6/view?usp=sharing"
        },
        {
          heading: "Python Fundamental for Data Science",
          color: "yellow lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1enaki0EBYiLfc412BUfYAXp3B2prAbgz/view?usp=sharing"
        },
        {
          heading: "Python for Data Professional Beginner - Part 3",
          color: "purple lighten-2",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1hy-zuJazztfpX2Rvnj_1i5d3A6cgDnLM/view?usp=sharing"
        },
        {
          heading: "Python for Data Professional Beginner - Part 2",
          color: "black lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1TLRrIP7-yTsGObin4ORutOKe7zjYlYVv/view?usp=sharing"
        },
        {
          heading: "Data Science Challenge with Python",
          color: "cyan lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/1mJ3wwZuoo2b9lxP8UKuQexOjz8LM-hOf/view?usp=sharing"
        },
        {
          heading: "Data Engineer Challenge with Python",
          color: "red lighten-1",
          content: "Sertifikat kelulusan dari DQLab.",
          link:
            "https://drive.google.com/file/d/13NUkAIkungbR_U_E-0bAOrlTsKJw4Woc/view?usp=sharing"
        }
      ]
    };
  }
};
</script>

