<template>
  <v-app id="inspire">
    <v-app-bar
      app
      color="white"
      flat
    >
      <v-container class="py-0 fill-height">
        <v-avatar
          class="mr-10"
          color="red lighten-3"
          size="52"
        ></v-avatar>

<v-toolbar-title>COE. Management</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-responsive max-width="220">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>

    <v-main class="red lighten-3">
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg">
              <v-list color="transparent">
                <v-list-item
                  @click="$router.push('/')"
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      Back to menu
                    </v-list-item-title>
                    <v-list-item-title>
                      ถอยกลับ
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider class="my-2"></v-divider>

                <v-list-item
                  link
                  color="grey lighten-4"
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      Refresh
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>

          <v-col>
            <v-sheet
              min-height="70vh"
              rounded="lg"
            >
            <v-card>
    <v-card-title>
      Management Data
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :search="search"
    ></v-data-table>
  </v-card>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>


  export default {
    data () {
      return {
        search: '',
        headers: [
          {
            text: 'Company',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Location', value: 'calories' },
          { text: 'Compensation', value: 'carbs' },
          { text: 'User', value: 'protein' },
          { text: 'Score', value: 'iron' },
        ],
        desserts: [
          {
            name: 'บริษัทฮา ไม่จำกัด',
            calories: 'กรุงเทพฯ',
            carbs: 'ได้',
            protein: 'Methee Heephong',
            iron: '99.9',
          },
          {
            name: 'บริษัทกำจัดขน',
            calories: 'ขอนแก่น',
            carbs: 'ไม่ได้',
            protein: 'มั่ง บางบัว',
            iron: '100',
          },
          
        ],
      }
    },
  }
</script>