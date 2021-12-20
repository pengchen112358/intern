<template>
  <v-app>
    <v-main> 
      <v-card class="overflow-hidden">
        <v-app-bar
          absolute
          elevate-on-scroll
          scroll-target="#scrolling-techniques-7"
          color="#8ECAE6">
        

        <v-btn plain href="#home" >
          <v-toolbar-title 
            style="color:#126782;font-family: Copperplate, Fantasy; font-size:20px"
          >Iot Control</v-toolbar-title>
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn 
          plain
          class="d-none d-sm-flex"
          href="#r1">
          Room 1
        </v-btn>
        
        <v-btn 
          class="d-flex d-sm-none"
          plain 
          dark 
          small
          icon 
          href="#r1"><v-icon>temple_buddhist</v-icon></v-btn>

        <v-btn 
          plain
          class="d-none d-sm-flex"
          href="#r2">
          Room 2
        </v-btn>

        <v-btn 
          class="d-flex d-sm-none"
          plain 
          dark 
          icon 
          small
          href="#r2"><v-icon>other_houses</v-icon></v-btn>

        <v-btn 
          plain
          class="d-none d-sm-flex"
          href="#r3">
          Room 3
        </v-btn>

        <v-btn 
          class="d-flex d-sm-none"
          plain 
          small
          dark 
          icon 
          href="#r3"><v-icon>home_work</v-icon></v-btn>

        </v-app-bar>
        <v-sheet
          id="scrolling-techniques-7"
          class="overflow-y-auto"
          max-height="2000px"
        >
          <div style="height:5000px">
            <v-row id="home" class="my-16 py-16 mx-16 d-none d-xs-flex d-md-flex ">
                <v-col
                  class="d-none d-lg-flex pt-16 "
                  cols="4">               
                    <v-icon class="d-none d-lg-flex py-16 my-10 " size="400px" color = "#FFB703">flutter_dash</v-icon>           
                </v-col>
                <v-col
                  cols = "12"
                  lg = "8"
                  >
                  <div >
                    <Home/>
                  </div>
                </v-col>
            </v-row>
            <Control/>
          </div>
          <div>
            
          </div>

        </v-sheet>
      </v-card>          
    </v-main>
  </v-app>
</template>

<style>
html {
  overflow: hidden !important;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

html::-webkit-scrollbar {
  width: 0;
  height: 0;
}
</style>

<script>
import Home from './components/Home';
import Control from './components/Control';


export default {
  name: 'App',

  components: {
    Home,
    Control,
  },

  data: () => ({

  }),

};
</script>
