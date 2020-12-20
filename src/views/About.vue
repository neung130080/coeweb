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
            <v-col cols="3" sm="2" md="2">
                <v-text-field
                  label="COE# ?"
                  required
                />
              </v-col>
              
              <v-col cols="25">
                <v-row>
               <v-col cols="4" sm="4" md="3">
                <v-text-field
                  label="ชื่อ / Name"
                  required
                />
              </v-col>
               <v-col cols="4" sm="4" md="3">
                <v-text-field
                  label="นามสกุล / Lastname"
                  required
                />
              </v-col>
              </v-row>
              </v-col>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>


  export default {
    data: () => ({
      links: [
        'COE. Management',
        
      ],
    }),
  }
</script>