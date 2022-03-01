<template>
  <div class="bg-white overflow-hidden shadow header">
    <div class="mt-4 mr-4 ml-4">
      <v-row colls="12">
        <v-col>
          <NuxtLogo/>
        </v-col>
        <v-col>
          <NuxtLink to="/">
              <button class="button exitbtn" depressed>Exit</button>
          </NuxtLink>
        </v-col>
      </v-row>
     </div>   
  </div>
</template>

<script>
import NuxtLogo from '../components/NuxtLogo'
export default {
  name: 'AppHeader'
}
</script>