<template>
  <div class="home" ref="home">
    <v-container fluid ma-0 pa-0 style="width: 100%;">
      <div :class="$vuetify.breakpoint.width > 1000 ? 'parallaxxx building1' : ''"></div>

    <v-container class="px-md-5" :style="`max-width: ${dynamicWidth}px`">
      <v-row>
        <v-col cols="12" md="6" class="px-0 pr-md-5">
          <div class="body-2 text-lg-body-1 text-justify mx-md-0 my-3" style="color: #09393d;">
            <span style="color: #BEAF67" class="font-weight-bold" v-text="englishOn ? dynamicHome1[1] : dynamicHome1[0]"></span> {{ englishOn ? dynamicHome2[1] : dynamicHome2[0] }}
          </div>
        </v-col>

        <v-col cols="12" md="6" class="px-0 pl-md-5">
          <h3 class="text-h6 text-md-h4 text-xl-h3 pa-md-2 px-md-0 px-xl-15 text-left animation" style="color: #BEAF67">{{ englishOn ? dynamicHome3[1] : dynamicHome3[0] }}</h3>
        </v-col>

      </v-row>
    </v-container>
  </v-container>
  </div>
</template>

<script>

export default {
  name: 'Home',
  props: ['dynamicWidth', 'englishOn'],
  data: function () {
      return {
        dynamicHome1: [
          'Köszöntjük honlapunkon',
          'Welcome to our website'
        ],
        dynamicHome2: [
          ', akkor is, ha csak véletlenül talált ránk és köszöntjük, ha célirányosan bennünket keresett.  Amit vállalunk: Önre és az ügyére koncentrálva a lehető leggyorsabban, szakmailag helytállóan fogunk dolgozni az Ön, a családja és a vállalkozása számára.',
          ', even if you only found us by chance or if you were looking for us directly! What we can offer: we will work as quickly and professionally as possible for you, your family or your business.'
        ],
        dynamicHome3: [
          'Jogi képviselet, több mint 25 év tapasztalattal',
          'Legal representation, with more then 25 years of experience!'
        ]
    }
  }
}
</script>
