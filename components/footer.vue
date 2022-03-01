<template>
  <div class="bg-white overflow-hidden shadow footer">
    <div class="mt-4 mr-4 ml-4">
        <NuxtLink to="/location">
            <button class="button backbtn" depressed>Back</button>
        </NuxtLink>
        
        <NuxtLink to="#">
            <button class="button nextbtn" depressed>Next</button>
        </NuxtLink>
    </div>
    
    <p class="mt-4 pt-2 text-gray-800 border-t"></p>
    <div class="ml-8 float-center">
        <v-row cols="12">
            <v-col> 
            <div class="underline"></div>
            </v-col>
            <v-col> 
            <div class="underline"></div>
            </v-col>
            <v-col> 
            <div class="underline"></div>
            </v-col>
        </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppFooter',
  props: ['link'],
  data () {
    return {
      
      // next: this.nextPage(),

    }
  },
  // methods: {
  //   nextPage(){
  //     if(this.activePage == "BedPage"){
  //       return {
  //         next:'/location',
  //       }
  //     }else if(this.activePage == "Region"){
  //       return {
  //         next:'/amenity',
  //       }
  //     }

  // },
  // }
}
</script>