<template>
  <div class="text-center">
    <v-hover v-slot:default="{ hover }" open-delay="50">
      <v-card :elevation="hover ? 8 : 0" class="" width="220">
        <v-img
          class="pointer-cursor"
          max-width="220"
          :src="productImage"
        ></v-img>

        <v-card-text class="text-start">
          <div class="font-weight-meduim black--text">{{ productName }}</div>
          <div class="font-weight-meduim primary--text">
            <span class="">{{ productPrice }} </span>
          </div>

          <div class="d-flex justify-space-between mt-2">
            <v-chip small label class="ma-0 white--text" color="primary">
              ສິນຄ້າດີ
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
</template>

<script>
import ProductImage from '~/assets/img/products/01.webp'
export default {
  name: 'discount-card',
  data() {
    return {
      productName: '#Honda #Accord 1.5 Turbo el ປີ 2021 ລົດງາມ',
      productPrice: '219000 LAK',
      discountPrice: '119000 LAK',
      discountPercent: '-50%',
      productImage: ProductImage,
    }
  },
}
</script>

<style></style>
