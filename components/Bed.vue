<!-- Please remove this file from your project -->
<template>
    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
        <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
        <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
        
            <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
                <h2 class="text-2xl leading-7 font-semibold">
                How many guests can can your place accommodate?
                </h2>

                <h3 class="mt-3 text-gray-600">
                Check that you have enough beds to accommodate all your guests confortably.
                </h3>
                <p class="mt-3 text-gray-600">
                </p>

                <v-container fluid>
                <v-row>
                    <v-col cols="12">
                  
                    </v-col>
                    <h3 class="mt-3 text-gray-600">
                    How many bedrooms can guests use?.
                    </h3>
                    <v-col cols="12">
                    <v-select
                        :placeholder="select"
                        :items="items"
                        outlined
                        dense
                    ></v-select>
                    </v-col>
                    <h3 class="mt-3 text-gray-600">
                    How many beds can guests use?.
                    </h3>
                    <v-col cols="12">
                    
                    </v-col>
                </v-row>
                </v-container>

                <p class="mt-4 pt-4 text-gray-800 border-t border-dashed">

                </p>
                
                <NuxtLink to="/"><v-btn depressed>Back</v-btn></NuxtLink>
                
                <NuxtLink to="/location"><v-btn depressed @click="saveBed()">Next</v-btn></NuxtLink>
            </v-btn>
            </div>
        </div>
    </div>
</template>

<script>
export default {
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
