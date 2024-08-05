<template>
  <div>
    <v-row justify="center" class="text-center mt-4">
      <v-col cols="12" sm="5">
        <v-divider class="grey"></v-divider>
      </v-col>
      <v-col cols="12" sm="2" ><h1 class="mt-n5">ຂາຍລົດ</h1> </v-col>
      <v-col cols="12" sm="5">
        <v-divider class="grey"></v-divider>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12" sm="6">
        <v-select :items="items" label="ຢີຫໍ້ລົດ" outlined dense></v-select>
      </v-col>

      <v-col cols="12" sm="6"
        ><v-select :items="items" label="ປະເພດລົດ" outlined dense></v-select>
      </v-col>
      <v-col cols="12" sm="6"
        ><v-select :items="items" label="ລຸ້ນລົດ" outlined dense></v-select>
      </v-col>
      <v-col cols="12" sm="6"
        ><v-select :items="items" label="ສີລົດ" outlined dense></v-select>
      </v-col>
      <v-col cols="12" sm="6"
        ><v-select :items="items" label="ປີຜະລິດລົດ" outlined dense></v-select>
      </v-col>
      <v-col cols="12" sm="6"
        ><v-text-field label="ລາຄາຂາຍ" outlined dense></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" sm="6">
        <h3 class="ma-2">ລົດໄຟຟ້າ</h3>
        <v-alert
          prominent
          outlined
          type="success"
          dense
          icon="mdi-car-connected"
        >
          <v-row align="center">
            <v-col class="grow"> ລົດໄຟຟ້າ </v-col>
            <v-col class="shrink">
              <v-switch
                v-model="ex11"
                color="success"
                value="success"
                hide-details
              ></v-switch>
            </v-col>
          </v-row>
        </v-alert>
      </v-col>
      <v-col cols="12" sm="6">
        <h3 class="ma-2">ລະບົບເກຍ</h3>
        <v-alert prominent outlined type="success" dense icon="mdi-car-clutch">
          <v-row align="center">
            <v-col class="grow"> ເກຍອໍໂຕ </v-col>
            <v-col class="shrink">
              <v-switch
                v-model="ex11"
                color="success"
                value="success"
                hide-details
              ></v-switch>
            </v-col>
          </v-row>
        </v-alert>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="" cols="12" sm="12">
        <v-file-input multiple outlined label="ຮູບລົດ"></v-file-input>
        <v-btn class="primary" large block> ໂພສຂາຍລົດ</v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
