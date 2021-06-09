<template>
  <div class="dashboard">
    <v-container fluid class="my-5">
      
      <v-card flat>
        <v-layout row wrap class="pa-3">
          <v-flex xs12 md10>
            <h1 class="subheading grey--text">Vehicles Dashboard</h1>
          </v-flex>
          
          <v-flex xs12 md2>
            
            <v-btn
                :loading="loading3"
                :disabled="loading3"
                color="blue-grey"
                class="ma-2 white--text"
                @click="loader = 'loading3'"
            >
                <v-icon
                    left
                    dark
                >
                    mdi-plus
                </v-icon>
                Filter List
                
            </v-btn>
          </v-flex>
        </v-layout>
      </v-card>

    </v-container>
   
  </div>
</template>

<script>
  export default {
    name: 'BarraDash',

  }
</script>

