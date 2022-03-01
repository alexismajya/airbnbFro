<template>
    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
        <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
        <div class="max-w-4xl mx-auto sm:px-6 lg:px-8 text-xl">

        <Header/>
        
         <span class="bar"><span class="barhtml c25"></span></span>

            <div class=" bg-white overflow-hidden shadow p-6">


                <h2 class=" mt-6 text-2xl leading-7 font-bold">
                How many guests can your place accommodate?
                </h2>

                <v-container fluid>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          Check that you have enough beds to accommodate all your guests confortably.
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <span class=" leading-5 font-semibold ">Guests</span>
                        <button class="circle ml-10" depressed >-</button>
                        <span class=" p-4 font-semibold">10</span>
                        <button class="circle" depressed >+</button>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          How many bedrooms can guests use?.
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="6">
                      <div class="mt-1 text-xl">
                        <v-select
                        :placeholder="select"
                        :items="items"
                        outlined
                    ></v-select>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          How many beds can guests use?.
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                       <div class="mt-4">
                        <span class=" leading-5 font-semibold ">Beds</span>
                        <button class="circle ml-10" depressed >-</button>
                        <span class=" p-4 font-semibold">1</span>
                        <button class="circle" depressed >+</button>
                      </div>
                    </v-col>
                </v-row>
                 <v-row>
                    <v-col cols="12">
                       <div class="mt-4">
                        <h2 class="text-2xl leading-7 font-semibold">
                          Sleeping arrangements
                        </h2>
                      </div>
                    </v-col>
                </v-row>
                 <v-row>
                    <v-col cols="12">
                       <div class="mt-2">
                        <h3 class="text-gray-600">
                          Sharing the types of beds in each room can help people understand the sleeping arrangements
                        </h3>
                      </div>
                    </v-col>
                </v-row>
                </v-container>

            </div>
            <div class="bg-white overflow-hidden shadow footer">
            <div class="mt-4 mr-4 ml-4">
              <v-row >
                <v-col colls="6">
                <NuxtLink to="/">
                    <button class="button backbtn flex " depressed><BackLogo/>Back</button>
                </NuxtLink>
                </v-col>
                <v-col colls="6">
                <NuxtLink to="/location">
                    <button class="button nextbtn mr-4" @click="saveBed()">Next</button>
                </NuxtLink>
                </v-col>
              </v-row>
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
        </div>
    </div>
</template>

<script>
import Footer from '../components/footer'
import Header from '../components/header'
export default {
  components: {
    Footer,
    Header
  },
  name: 'Bed',
  data () {
    return {
      select: 'Studio',
      items: [
        'Studio',
        'Shared room',
        'Single room',
      ],
    }
  },
  methods: {
    async saveBed(){
    try{
      const res = await this.$axios.post('addRoom', {'roomType': 'studio', 'guests': 10, 'beds': 2 })
      console.log(res)
    }
    catch(e){
      console.log(e.message)
    }

  },
  }
}
</script>
