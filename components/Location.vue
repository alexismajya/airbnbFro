<template>
    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
        <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
        <div class="max-w-4xl mx-auto sm:px-6 lg:px-8 text-xl">

        <Header/>
        
         <span class="bar"><span class="barhtml c50"></span></span>

            <div class=" bg-white overflow-hidden shadow p-6">


                <h2 class=" mt-6 text-2xl leading-7 font-bold">
                Where your place located?
                </h2>

                <v-container fluid>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          Guests will only get your exact address once they've booked reservation.
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-1">
                        <button class="locbtn" depressed > Use current location</button>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="4">
                      <div class="mt-1">
                        <p class="mt-4 text-gray-800 border-t"></p>
                      </div>
                    </v-col>
                     <v-col cols="4">
                      <div class="mt-1">
                        <p class="text-gray-400 text-semibold">or enter your address</p>
                      </div>
                    </v-col>
                    <v-col cols="4">
                      <div class="mt-1">
                        <p class="mt-4 text-gray-800 border-t"></p>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-2">
                        <h3 class="text-gray-600 text-xl">
                          Country / Region  
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-0 text-gray-600 text-xl">
                        <v-select
                        :placeholder="select"
                        :items="regions"
                        outlined
                    ></v-select>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-2">
                        <h3 class="text-gray-600 text-xl">
                          Street address
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                       <div class="mt-0 text-xl">
                        <v-text-field
                            placeholder="House name/number + street/road"
                            outlined
                            
                        ></v-text-field>
                      </div>
                    </v-col>
                </v-row>
                 <v-row>
                    <v-col cols="12">
                       <div class="mt-2">
                        <h3 class="text-gray-600">
                          Apt, suite. (optional)
                        </h3>
                      </div>
                    </v-col>
                </v-row>
                 <v-row>
                    <v-col cols="12">
                       <div>
                        <v-text-field class="mt-0 text-xl pt-4"
                            placeholder="Apt., suite, building access code"
                            outlined
                            
                        ></v-text-field>
                      </div>
                    </v-col>
                </v-row>
                </v-container>

            </div>
            <div class="bg-white overflow-hidden shadow footer">
            <div class="mt-4 mr-4 ml-4">
                <v-row >
                <v-col colls="6">
                <NuxtLink to="/bed">
                    <button class="button backbtn flex " depressed><BackLogo/>Back</button>
                </NuxtLink>
                </v-col>
                <v-col colls="6">
                <NuxtLink to="/amenity">
                    <button class="button nextbtn mr-4">Next</button>
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
import BackLogo from '../components/BackLogo.vue'
export default {
  name: 'Location',
  data () {
    return {
      select: 'Rwanda', 
      $myActivePage: 'Region',
      regions: [
        'Rwanda',
        'Burundi',
        'Kenya',
      ],
    }
  },
 
}
</script>
