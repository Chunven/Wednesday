<template>
  <v-app>
    <div>
      <v-app-bar color="white" class="mb-2" elevation="0">
        <h3>APP NAME & LOGO</h3>
        <v-col class="d-flex justify-space-around">
          <div class="align-center">
            <v-btn text to="/">ໜ້າຫຼັກ</v-btn>
            <v-btn text to="">ລົດມືສອງ</v-btn>
            <v-menu open-on-hover offset-y transition="scale-transition">
              <template v-slot:activator="{ on }">
                <v-btn text v-on="on">
                  ຢີ່ຫໍ້ລົດ <v-icon>mdi-menu-down</v-icon>
                </v-btn>
              </template>
              <v-list>
                <v-list-item to="">
                  <v-list-item-title>Toyota</v-list-item-title>
                </v-list-item>
                <v-list-item to="">
                  <v-list-item-title>Honda</v-list-item-title>
                </v-list-item>
                <v-list-item to="">
                  <v-list-item-title>Izusu</v-list-item-title>
                </v-list-item>
                <v-list-item to="">
                  <v-list-item-title>Mazda</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
            <v-btn text to="">ອັບເດດລາຄາ</v-btn>
            <v-btn text to="">ຕິດຕໍ່ພວກເຮົາ</v-btn>

            <v-btn outlined color="green" height="45">
              <v-icon class="mr-2 mt-1">mdi-car-side</v-icon> ຂາຍລົດຂອງທ່ານ
            </v-btn>
            <v-btn class="ml-2" outlined color="primary" height="45">
              <v-icon class="mr-2 mt-1">mdi-login</v-icon> ເຂົ້າສູ່ລະບົບ
            </v-btn>
          </div>
        </v-col>
      </v-app-bar>
      <v-divider></v-divider>
    </div>

    <v-main>
      <Nuxt class="container pl-16 pr-16" />
    </v-main>

    <v-divider></v-divider>

    <v-footer padless class="white container pl-16 pr-16">
      <v-container>
        <v-row>
          <v-col cols="12" sm="4" md="4">
            <div>
              <h3>APP NAME & LOGO</h3>
              <h4 class="grey--text pa-4">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec maximus tellus non tincidunt ornare.
              </h4>
            </div>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <h3>ແຜ່ນທີ່ຮ້ານ</h3>
            <div>
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15180.260562408257!2d102.63310405!3d17.9757061!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x312468787e60ba55%3A0xb2e98d79c0280739!2z4Liq4LiW4Liy4LiZ4LmA4Lit4LiB4Lit4Lix4LiE4Lij4Lij4Liy4LiK4LiX4Li54LiV4LmE4LiX4Lii!5e0!3m2!1sth!2sla!4v1710425235808!5m2!1sth!2sla"
                width="400"
                height="200"
                style="border: 0"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
              ></iframe>
            </div>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <h3>ຕິດຕໍ່ພວກເຮົາ</h3>
            <div class="text-start" style="margin-left: -16px">
              <v-list-item>
                <v-list-item-content>
                  <span>
                    <v-icon>mdi-map-marker</v-icon> 013 ຖະໜົນ ສຸພານຸວົງ ບ້ານ
                    ສີຫອມ ເມືອງ ຈັນທະບູລີ ນະຄອນຫຼວງວຽງຈັນ ສປປ ລາວ</span
                  >
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <span>
                    <v-icon>mdi-phone</v-icon> 1698, (+856-21) 241275</span
                  >
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <span>
                    <v-icon>mdi-calendar-clock</v-icon> ວັນຈັນ - ວັນສຸກ, ເວລາ 8:30 - 17:30</span
                  >
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <a href="https://facebook.com" class="text-decoration-none"
                    ><v-icon>mdi-facebook</v-icon> Facebook Page</a
                  >
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <a
                    href="https://api.whatsapp.com/send?phone=2078989930"
                    class="text-decoration-none"
                    ><v-icon>mdi-whatsapp</v-icon> Whatsapp Store</a
                  >
                </v-list-item-content>
              </v-list-item>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      socialIcon: [
        {
          title: 'facebook',
          path: '',
          icon: 'mdi-facebook',
          color: 'blue',
        },
        {
          title: 'tiktok',
          path: '',
          icon: 'mdi-music-note-eighth',
          color: 'grey',
        },
        {
          title: 'instragram',
          path: '',
          icon: 'mdi-instagram',
          color: 'purple',
        },
      ],
    }
  },
}
</script>

<style></style>
