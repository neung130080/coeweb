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

        <v-btn
          v-for="link in links"
          :key="link"
          text
        >
          {{ link }}
        </v-btn>

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
                  @click="$router.push('about')"
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      Add management
                    </v-list-item-title>
                    <v-list-item-title>
                      เพิ่มข้อมูลการทำงาน
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item
                  link
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      Management 
                    </v-list-item-title>
                    <v-list-item-title>
                      ดูข้อมูลการทำงาน
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
            <div style="text-align:center;">
              <br />
      <h2>COE. Student Employment</h2>
      <h2>Management System</h2>
      <br />
      <p>
        สาขาวิศวกรรมคอมพิวเตอร์ คณะวิศวกรรมศาสตร์
        <br />มหาวัทยาลัยราชภัฏมหาสารคาม
        <br />
      </p>
    </div>
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