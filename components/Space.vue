<template>
  <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
    <div class="max-w-4xl  mx-auto sm:px-6 lg:px-8 text-xl">
      <Header/>
      <div class=" bg-white overflow-hidden shadow p-6 maxH ">
        <h1 class="text-2xl font-semibold">
          Let's get started listing your space.
        </h1>

         <h3 class="mt-3 text-gray-400">
          STEP 1
        </h3>
         <h2 class="text-2xl  font-semibold">
          What king of place do you have?
        </h2>
        <p class="mt-3 text-gray-600">
        </p>
        <v-container fluid>
          <v-row>
            <v-col
              cols="12" class="mt-0 text-xl"
            >
              <v-select
                :placeholder="select"
                :items="items"
                outlined
                dense
               ></v-select>
            </v-col>
            <v-col
              cols="12" class="mt-0 text-xl"
            >
              <v-select
                :placeholder="select2"
                :items="guests"
                outlined
                dense
               ></v-select>
            </v-col>
            <v-col cols="12" class="mt-0 text-xl">
              <v-text-field
                :placeholder="region"
                outlined
                dense
              ></v-text-field>
            </v-col>
          </v-row>
          
          <NuxtLink to="/bed">
            <button class="button bigWidth" depressed right @click="saveSpace()" >
              Continue
            </button>
          </NuxtLink>
        
        </v-container>
        <div class="bg-white overflow-hidden shadow footer">
          <p class="mt-4 pt-4 text-gray-800 border-t">
          </p>
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
export default {
  name: 'Space',
  data () {
    return {
      select: 'Private room',
      select2: 'for 10 guests',
      items: [
        'Private room',
        'Shared room',
        'Entire place',
      ],
      guests: [
        'for 10 guests',
        'for 5 guests',
        'for 1 guest',
      ],
      region: 'Kigali, Rwanda',
    }
  },
  methods: {
    async saveSpace(){
    try{
      const res = await this.$axios.post('add/', {'description': 'Private room', 'guests': 10, 'region': 'Kigali/Rwanda' })
      console.log(res)
    }
    catch(e){
      console.log(e.message)
    }

  },
  }
}
</script>
