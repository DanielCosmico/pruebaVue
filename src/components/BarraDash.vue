<template>
  <div class="dashboard">
    <v-container fluid class="my-5">

      <v-row class="text-left">

          <v-col cols='10'>
            <v-row>
              <h1>Vehicles Dashboard</h1>
              <p class="ml-3 mt-4" > 1192 total</p>
            </v-row>
              
          </v-col>

          <v-col cols='2'>  
            <v-btn
                :loading="loading3"
                :disabled="loading3"
                color="blue-grey"
                class="ma-2 white--text"
                @click="loader = 'loading3'">
                <v-icon
                    left
                    dark>
                    mdi-plus
                </v-icon>
                Filter List  
            </v-btn>
          </v-col>

      </v-row >

    </v-container>
  </div>
</template>

<script>
  export default {
    name: 'BarraDash',

  }
</script>

