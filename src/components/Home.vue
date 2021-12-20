<template>
  <div>
    <v-container  >
      <v-row>
        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
          md="4"
        >
          <v-hover v-slot="{ hover }">        
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
              :color="item.color"
              dark
            >
              <div class="align-self-center">
                <v-card-actions>
                  <v-row no-gutters>
                    <v-col 
                      col="12"
                      >
                      <v-card-title
                        class="text-h1 align-end d-none d-lg-flex"
                        v-text="item.title"
                        :color="item.btncolor"
                      ></v-card-title>
                    </v-col>
                    <v-card-title
                        class="text-h3 align-end d-md-flex d-xs-flex d-lg-none"
                        v-text="item.title"
                        :color="item.btncolor"
                      ></v-card-title>
                    <v-col
                      col="12"
                      >
                      <v-btn
                        class="ml-2 mt-5"
                        :class="{ 'show-btns': hover }"
                        outlined
                        rounded
                        small
                        :color="item.btncolor"
                        :href="item.id"
                      >
                        ENTER
                      </v-btn>
                    </v-col>                   
                  </v-row>
                </v-card-actions>
              </div>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}

.a {
  color: aliceblue;
}
</style>

<script>
  export default {
    data: () => ({
      items: [
        {
          id:'#r1',
          color: '#8ECAE6',
          title: 'Room 1',
          btncolor: '#126782',
        },
        {
          id:'#r2',
          color: '#FFB703',
          title: 'Room 2',
          btncolor: '#FB8500',

        },
        {
          id:'#r3',
          color: '#8ECAE6',
          title: 'Room 3',
          btncolor: '#126782',
        },
      ],
    }),
  }
</script>