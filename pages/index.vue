<template>
  <div>
    <!-- carousel -->
    <v-row justify="center">
      <v-col cols="12" sm="12" md="12">
        <v-carousel v-model="model" height="500" hide-delimiter-background>
          <v-carousel-item
            v-for="(image, index) in carouselImages"
            :key="index"
          >
            <img
              :src="image"
              width="100%"
              style="max-height: 500px; object-fit: cover"
            />
          </v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>
    <!-- big two button -->
    <v-row class="mt-4">
      <v-col cols="12" sm="6" md="6">
        <v-btn block color="orange" class="white--text rounded-lg" height="70">
          <v-icon class="mr-2" size="40">mdi-car-2-plus</v-icon>
          <div style="font-size: 25px">ຊື້ລົດມືສອງ</div>
        </v-btn>
      </v-col>
      <v-col cols="12" sm="6" md="6">
        <v-btn block color="green" class="white--text rounded-lg" height="70">
          <v-icon class="mr-2" size="40">mdi-car-arrow-right</v-icon>
          <div style="font-size: 25px">ຂາຍລົດຂອງທ່ານ</div>
        </v-btn>
      </v-col>
    </v-row>
    <!-- promotion section -->
    <div class="discount-promotion mb-4 mt-6">
      <v-card class="pa-6 rounded-lg">
        <v-row>
          <v-list class="" style="margin-bottom: -10px">
            <v-list-item>
              <v-avatar tile color="green rounded-pill" size="40" class="mr-2">
                <v-icon color="white">mdi-cash-minus</v-icon></v-avatar
              >
              <v-list-item-title> <h3>ລົດຫຼຸດລາຄາພິເສດ</h3> </v-list-item-title>
              <v-list-item-icon> </v-list-item-icon>
            </v-list-item>
          </v-list>
          <v-spacer />
          <v-btn text color="green" class="green--text mt-3">
            ເບິ່ງເພີ່ມເຕີມ
            <v-icon right dark> mdi-arrow-right-circle </v-icon>
          </v-btn>

          <v-col cols="12">
            <v-divider class="mb-2"></v-divider>
            <div class="row">
              <div
                v-for="(item, index) in 12"
                :key="index"
                class="col-12 col-md-2 col-sm-6 col-xs-6 text-center"
              >
                <discount-card></discount-card>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-card>
    </div>
    <!-- good product section -->

    <div class="good-product-promotion mb-4 mt-6">
      <v-card class="pa-6 rounded-lg">
        <v-row>
          <v-list class="" style="margin-bottom: -10px">
            <v-list-item>
              <v-avatar
                tile
                color="primary rounded-pill"
                size="40"
                class="mr-2"
              >
                <v-icon color="white">mdi-thumb-up</v-icon></v-avatar
              >
              <v-list-item-title> <h3>ລົດຄຸນນະພາບດີ</h3> </v-list-item-title>
              <v-list-item-icon> </v-list-item-icon>
            </v-list-item>
          </v-list>
          <v-spacer />
          <v-btn text color="primary" class="primary--text mt-3">
            ເບິ່ງເພີ່ມເຕີມ
            <v-icon right dark> mdi-arrow-right-circle </v-icon>
          </v-btn>

          <v-col cols="12">
            <v-divider class="mb-2"></v-divider>
            <div class="row">
              <div
                v-for="(item, index) in 12"
                :key="index"
                class="col-12 col-md-2 col-sm-6 col-xs-6 text-center"
              >
                <good-product-card></good-product-card>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-card>
    </div>

    <!-- list item -->
    <v-row>
      <v-col v-for="n in 4" :key="n" cols="12" sm="3" md="3" class="">
        <v-card-title>
          <a href="/car-toyota" title="ຂາຍລົດ Toyota ມືສອງ ສະພາຍດີ"
            >ຂາຍລົດ Toyota ມືສອງ ສະພາບດີ</a
          >
        </v-card-title>
        <v-list>
          <v-list-item v-for="(item, index) in toyotaCars" :key="index">
            <v-list-item-content>
              <v-list-item-title>
                <a :href="item.link" :title="item.title">{{ item.title }}</a>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import carouselImage1 from '~/assets/img/carousel/1.png'
import carouselImage2 from '~/assets/img/carousel/2.png'

export default {
  data() {
    return {
      carouselImages: [carouselImage1, carouselImage2],
      toyotaCars: [
        { link: '/car-toyota-fortuner', title: 'ລົດ fortuner ມືສອງ' },
        { link: '/car-toyota-yaris', title: 'ລົດ yaris ມືສອງ' },
        { link: '/car-toyota-vios', title: 'ລົດ vios ມືສອງ' },
        { link: '/car-toyota-hilux-vigo', title: 'ລົດ hilux-vigo ມືສອງ' },
        { link: '/car-toyota-camry', title: 'ລົດ camry ມືສອງ' },
      ],
    }
  },
}
</script>

<style>
a,
u {
  text-decoration: none;
}
</style>
