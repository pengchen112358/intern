<template>
  <v-item-group multiple>
    <v-container>
    <v-row 
        no-gutters 
        class="mt-16 py-16 my-16"
        v-for="(room, j) in Rooms"
        :key="j"
        :id="room.id">

        <v-col 
            class="mx-auto my-auto"
            cols="12"
            lg="6">
        <h1 
            class="font-weight-bold my-16"
            style="background-color: #8ECAE6;color:white; padding:20px"
            color="#8ECAE6"
            v-text="room.title"
        ></h1>
            <v-row
             v-for="r in room.row"
             :key="r"
             >
                <v-col
                v-for="c in r.col"
                :key="c"
                class="justify-space-between mb-6"
                cols="4"
                md="4"
                >
                <h4
                  class="font-weight-light my-auto"
                >{{c.thing}}</h4>
                <v-item v-slot="{ active, toggle }">
                    <v-btn
                    :color="active ? '#8ECAE6' : '#BDBDBD'"
                    class="align-center"
                    dark
                    x-large
                    @click="toggle"
                    >
                        
                        <v-icon>{{ c.btn }}</v-icon>
                        
                        
                    </v-btn>
                    
                </v-item>
                </v-col>
            </v-row>
        </v-col>
        <v-col
            class="d-none d-lg-flex "
            cols="6">
            <v-icon 
              class="d-none d-lg-flex ma-auto pt-16" 
              size="400px" 
              color = "#FFB703"
            >{{room.pic}}</v-icon>

        </v-col>
    </v-row>
    </v-container>
  </v-item-group>
</template>


<script>
  export default {
    data: () => ({
      Rooms: [
        {
          id: 'r1',
          title: 'Room 1',
          pic:'temple_buddhist',
          row:[
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'front1',
                },
                                {
                  btn:'lightbulb',
                  thing:'front',
                },
                                {
                  btn:'lightbulb',
                  thing:'back1',
                },
              ],
            },
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'back2',
                },
                                {
                  btn:'lightbulb',
                  thing:'back3',
                },
                                {
                  btn:'lightbulb',
                  thing:'back4',
                },
              ],
            },
            {
              col:[
                {
                  btn:'desktop_windows',
                  thing:'desktop001',
                },
                                {
                  btn:'desktop_windows',
                  thing:'desktop002',
                },
                                {
                  btn:'desktop_windows',
                  thing:'desktop003',
                },
              ],
            },
          ],
        },
        {
          id:'r2',
          title: 'Room 2',
          pic:'other_houses',
          row:[
            {
              col:[
                {
                  btn:'desktop_windows',
                  thing:'Screen_left',
                },
                                {
                  btn:'desktop_windows',
                  thing:'Screen_up',
                },
                                {
                  btn:'desktop_windows',
                  thing:'Screen_mid',
                },
              ],
            },
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'left1',
                },
                                {
                  btn:'lightbulb',
                  thing:'left2',
                },
                                {
                  btn:'lightbulb',
                  thing:'left3',
                },
              ],
            },
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'right1',
                },
                                {
                  btn:'lightbulb',
                  thing:'right2',
                },
                                {
                  btn:'lightbulb',
                  thing:'right3',
                },
              ],
            },
          ],
        },
        {
          id:'r3',
          title: 'Room 3',
          pic:'home_work',
          row:[
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'big1',
                },
                                {
                  btn:'lightbulb',
                  thing:'big2',
                },
                                {
                  btn:'lightbulb',
                  thing:'big3',
                },
              ],
            },
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'top1',
                },
                                {
                  btn:'lightbulb',
                  thing:'top2',
                },
                                {
                  btn:'lightbulb',
                  thing:'top3',
                },
              ],
            },
            {
              col:[
                {
                  btn:'lightbulb',
                  thing:'small1',
                },
                                {
                  btn:'lightbulb',
                  thing:'small2',
                },
                                {
                  btn:'lightbulb',
                  thing:'small3',
                },
              ],
            },
          ],          
        },
      ],
    }),
  }
</script>