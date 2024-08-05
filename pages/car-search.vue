<template>
  <div>
    <v-row>
      <v-col cols="12" sm="6">
        <v-card class="pa-2">
          <v-card-text>
            <v-list class="">
              <v-list-item class="ml-n4">
                <v-avatar color="primary rounded-pill" size="30" class="mr-2">
                  <v-icon color="white">mdi-magnify</v-icon></v-avatar
                >
                <v-list-item-title> <h3>ຄົ້ນຫາລົດ</h3> </v-list-item-title>
              </v-list-item>
            </v-list>

            <v-row>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ຢີຫໍ້ລົດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ລຸ້ນລົດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ລາຄາຕ່ຳສູດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ລາຄາສູງສຸດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ປີເກົ່າສຸດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="6">
                <v-select
                  :items="items"
                  label="ປີໃໝ່ສຸດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
              <v-col class="" cols="12" sm="12">
                <v-select
                  :items="items"
                  label="ປະເພດລົດ"
                  outlined
                  dense
                ></v-select>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" sm="12">
                <p>ລະບົບເກຍ</p>
                <v-row>
                  <v-col cols="6">
                    <v-btn outlined color="blue" block> ເກຍອໍໂຕ </v-btn>
                  </v-col>
                  <v-col cols="6">
                    <v-btn outlined color="grey" block> ເກຍກະປຸກ </v-btn>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
            <v-row>
              <v-col class="" cols="12" sm="12">
                <v-btn class="primary" block>
                  <v-icon class="mr-2">mdi-magnify</v-icon> ຄົ້ນຫາລົດ</v-btn
                >
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card class="pa-2 mt-2 mb-2" v-for="(item, index) in 4" :key="index">
          <v-row>
            <v-col cols="12" sm="4">
              <v-img
                class="pointer-cursor"
                max-width="300"
                :src="productImage"
              ></v-img>
            </v-col>
            <v-col cols="12" sm="8">
              <v-card-text class="text-start">
                <h2 class="black--text">
                  {{ productName }}
                </h2>

                <div class="font-weight-meduim primary--text mt-4">
                  <h3 class="">{{ productPrice }}</h3>
                </div>
                <div class="font-weight-meduim orange--text mt-4">
                  <h3 class="">
                    <v-icon class="mr-2" color="orange"
                      >mdi-calendar-month</v-icon
                    >{{ ProductYear }}
                  </h3>
                </div>
                <div class="mt-4">
                  <v-btn small class="white--text" color="green">
                    ຕິດຕໍ່ Whatsapp
                  </v-btn>
                </div>
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import ProductImage from '~/assets/img/products/01.webp'
export default {
  data() {
    return {
      items: ['Toyota', 'Hyundai', 'Ford', 'Benz'],
      productName:
        ' 2024 Mercedes-Benz GLC350e 2.0 4MATIC AMG Dynamic 31.2 kWh SUV ລົດສະພາບດີ ມືສອງ',
      productPrice: '219000 LAK',
      productImage: ProductImage,
      ProductYear: '2016',
    }
  },
}
</script>

<style></style>
