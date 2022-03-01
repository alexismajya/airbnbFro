<template>
    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
        <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
        <div class="max-w-4xl mx-auto sm:px-6 lg:px-8 text-xl">

        <Header/>
        
         <span class="bar"><span class="barhtml c75"></span></span>

            <div class=" bg-white overflow-hidden shadow p-6">


                <h2 class=" mt-6 text-2xl leading-7 font-bold">
                What amenities do you offer?
                </h2>

                <v-container fluid>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          These are just the amenities guests usually expect, but you can add even more after you publish.
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class="mt-4">
                        <h3 class="text-gray-600">
                          Essentials
                        </h3>
                      </div>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="12">
                      <div class=" float-left">
                        <h3 class="text-gray-600">
                          Towels, bed sheets, soap, toilet paper, and pillows
                        </h3>
                      </div>
                      <div class="float-right">
                         <button class="button circle amenityCir" depressed></button>
                      </div>
                    </v-col>
                  </v-row>
                  <div class="mt-4">
                      <p class="mt-4 pt-2 text-gray-800 border-t"></p>
                 </div>
                 <v-row>
                    <v-col cols="12">
                      <div class=" mt-4 float-left">
                        <h3 class="text-gray-600">
                          Wifi
                        </h3>
                      </div>
                      <div class="mt-4 float-right">
                         <button class="button circle amenityCir" depressed></button>
                      </div>
                    </v-col>
                  </v-row>
                  <div class="mt-4">
                      <p class="mt-4 pt-2 text-gray-800 border-t"></p>
                 </div>
                 <v-row>
                    <v-col cols="12">
                      <div class=" mt-4 float-left">
                        <h3 class="text-gray-600">
                          TV
                        </h3>
                      </div>
                      <div class="mt-4 float-right">
                         <button class="button circle amenityCir" depressed></button>
                      </div>
                    </v-col>
                  </v-row>
                  <div class="mt-4">
                      <p class="mt-4 pt-2 text-gray-800 border-t"></p>
                 </div>
                 <v-row>
                    <v-col cols="12">
                      <div class=" mt-4 float-left">
                        <h3 class="text-gray-600">
                         Heat
                        </h3>
                      </div>
                      <div class="mt-4 float-right">
                         <button class="button circle amenityCir" depressed></button>
                      </div>
                    </v-col>
                  </v-row>
                  <div class="mt-4">
                      <p class="mt-4 pt-2 text-gray-800 border-t"></p>
                 </div>
                </v-container>

            </div>
            <div class="bg-white overflow-hidden shadow footer">
            <div class="mt-4 mr-4 ml-4">
                <v-row >
                <v-col colls="6">
                <NuxtLink to="/location">
                    <button class="button backbtn flex " depressed><BackLogo/>Back</button>
                </NuxtLink>
                </v-col>
                <v-col colls="6">
                <NuxtLink to="/#">
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
export default {
  name: 'Amenity',
  data () {
    return {
    
    }
  },
}
</script>
