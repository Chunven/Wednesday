<template>
  <div>
    <v-row>
      <v-breadcrumbs :items="items">
        <template v-slot:divider>
          <v-icon>mdi-arrow-right-thin</v-icon>
        </template>
      </v-breadcrumbs>
    </v-row>
    <v-row no-gutters class="mt-2">
      <v-col cols="12" sm="7">
        <v-row no-gutters>
          <v-col cols="12" sm="3">
            <v-list>
              <v-list-item v-for="(image, index) in productImages" :key="index">
                <v-img
                  height="100px"
                  :src="image"
                  alt="Thumbnail Image"
                  aspect-ratio="1"
                  @click="selectedThumbnail = index"
                  :class="{
                    'selected-thumbnail': selectedThumbnail === index,
                  }"
                />
              </v-list-item>
            </v-list>
          </v-col>
          <v-col cols="12" sm="9" class="mt-2">
            <v-carousel
              hide-delimiters
              v-model="selectedThumbnail"
              height="100%"
            >
              <v-carousel-item
                v-for="(image, index) in productImages"
                :key="index"
                :value="index"
              >
                <img
                  :src="mainImage"
                  width="100%"
                  height="600px"
                  alt="Main Image"
                  contain
                />
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" sm="5">
        <div class="ml-2">
          <h1 class="">
            2024 Mercedes-Benz GLC350e 2.0 4MATIC AMG Dynamic 31.2 kWh SUV
            ລົດສະພາບດີ ມືສອງ
          </h1>
          <v-divider class="mb-6 mt-6"></v-divider>
          <div class="">
            <v-row>
              <v-col cols="6" md="12" sm="12">
                <v-list-item>
                  <v-list-item-content>
                    <h3 class="mb-6">ລາຄາ: <b>35.000 USD</b></h3>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item>
                  <v-list-item-content class="">
                    <h3 class="mb-6">ຄຸນສົມບັດລົດ</h3>
                    <span>
                      Lorem Ipsum is simply dummy text of the printing and
                      <br /><br />
                      typesetting industry. Lorem Ipsum has been the industry's
                      <br /><br />
                      standard dummy text ever since the 1500s, when an unknown
                      <br /><br />
                      printer took a galley of type and scrambled it to make a
                      type specimen book.
                    </span>
                  </v-list-item-content>
                </v-list-item></v-col
              >
            </v-row>
          </div>
          <v-divider class="mb-6 mt-6"></v-divider>
          <v-row>
            <v-col cols="12" md="12" sm="12">
              <div class="ma-2">
                <v-row align="center" class="social-link">
                  <v-col cols="12" sm="12">
                    <span>ແບ່ງປັນຜ່ານ:</span>
                    <v-btn icon x-large color="blue">
                      <v-icon>mdi-facebook</v-icon>
                    </v-btn>
                    <v-btn icon x-large color="green">
                      <v-icon>mdi-whatsapp</v-icon>
                    </v-btn>
                  </v-col>
                </v-row>
              </div>
              <div class="buy-product">
                <v-col cols="12" sm="6" md="6">
                  <div class="mt-4">
                    <v-btn block class="ml-n2 white--text" color="green">ຕິດຕໍ່ Whatsapp</v-btn>
                  </div>
                </v-col>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
    <!-- title category -->
    <v-row justify="center" class="text-center mt-4">
      <v-col cols="12" sm="4" md="5">
        <v-divider class="grey"></v-divider>
      </v-col>
      <v-col cols="12" sm="4" md="2"
        ><h1 class="mt-n5">ລົດລຸ້ນດຽວກັນ</h1>
      </v-col>
      <v-col cols="12" sm="4" md="5">
        <v-divider class="grey"></v-divider>
      </v-col>
    </v-row>
    <!-- car recommmend -->
    <div class="mb-4 mt-6">
      <v-row>
        <v-col cols="12">
          <div class="row">
            <div
              v-for="(item, index) in 12"
              :key="index"
              class="col-12 col-md-2 col-sm-6 col-xs-6 text-center"
            >
              <div class="text-center">
                <v-hover v-slot:default="{ hover }" open-delay="50">
                  <v-card :elevation="hover ? 8 : 0" class="" width="220">
                    <v-img
                      class="pointer-cursor"
                      max-width="220"
                      :src="productImage"
                    ></v-img>

                    <v-card-text class="text-start">
                      <div class="font-weight-meduim black--text">
                        {{ productName }}
                      </div>
                      <div class="font-weight-meduim primary--text">
                        <span class="">{{ productPrice }} </span>
                      </div>

                      <div class="d-flex justify-space-between mt-2">
                        <v-chip
                          small
                          label
                          class="ma-0 white--text"
                          color="primary"
                        >
                          ແນະນຳ
                        </v-chip>
                        <v-spacer></v-spacer>
                        <v-chip
                          small
                          label
                          outlined
                          class="ma-0 primary--text"
                          color="primary"
                        >
                          ຕິດຕໍ່ Whatsapp
                        </v-chip>
                      </div>
                    </v-card-text>
                  </v-card>
                </v-hover>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
import ProductImage01 from '~/assets/img/products/2.webp'
import ProductImage02 from '~/assets/img/products/3.webp'
import ProductImage03 from '~/assets/img/products/4.webp'
import ProductImage from '~/assets/img/products/01.webp'

export default {
  data: () => ({
    productName: '#Honda #Accord 1.5 Turbo el ປີ 2021 ລົດງາມ',
    productPrice: '219000 LAK',
    discountPrice: '119000 LAK',
    discountPercent: '-50%',
    productImage: ProductImage,
    productImages: [ProductImage01, ProductImage02, ProductImage03],
    items: [
      {
        text: 'ໜ້າຫຼັກ',
        disabled: false,
        href: 'Index',
      },
      {
        text: 'ສິນຄ້າທັງໝົດ',
        disabled: false,
        href: 'all-product',
      },
      {
        text: '2024 Mercedes-Benz GLC350e 2.0 4MATIC AMG Dynamic 31.2 kWh SUV ລົດສະພາບດີ ມືສອງ',
        disabled: true,
        href: '/',
      },
    ],
    quantity: 1, // Initial quantity value
    selectedThumbnail: 0, // Initially selected thumbnail
  }),

  methods: {
    changeQuantity: function (num) {
      this.quantity += +num
      console.log(this.quantity)
      !isNaN(this.quantity) && this.quantity > 0
        ? this.quantity
        : (this.quantity = 0)
    },
  },
  computed: {
    mainImage() {
      return this.productImages[this.selectedThumbnail]
    },
  },
}
</script>

<style>
/* Product Quantity */
.wrapper {
  height: 40px;
  display: flex;
}
.quantity {
  border: none;
  text-align: center;
  width: 70px;

  font-size: 16px;
  color: #43484d;
  font-weight: 300;
  border: 1px solid #e1e8ee;
}

.btn {
  border: 1px solid #e1e8ee;
  width: 50px;
  background-color: #e1e8ee;
  /*   border-radius: 6px; */
  cursor: pointer;
}
button:focus,
input:focus {
  outline: 0;
}

.selected-thumbnail {
  border: 2px solid #3498db;
}
</style>
