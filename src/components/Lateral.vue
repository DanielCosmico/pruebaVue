<template>
  <v-card outlined class="pa-5" >
    <v-container fluid class="my-5">
        <v-layout row wrap >
            <v-flex xs12 md6>
                <p>Trips taken</p>
            </v-flex>
            <v-flex xs12 md6>
                <p>{{width}}</p>
            </v-flex>
        </v-layout>
    </v-container>
    
    <v-slider
      v-model="width"
      class="align-self-stretch"
      min="200"
      max="500"
      step="1"
      color="#2e5bff"
    ></v-slider>

    <v-container fluid class="my-5">
        <v-layout row wrap >
            <v-flex xs12 md6>
                <p>Service due</p>
            </v-flex>
            <v-flex xs12 md6>
                <p>{{service}}</p>
            </v-flex>
        </v-layout>
    </v-container>
    <v-slider
      v-model="service"
      class="align-self-stretch"
      min="0"
      max="30"
      step="1"
      color="#2e5bff"
    ></v-slider>
    <p>Vehicle model</p>
    <v-combobox
        multiple
        label="Vehicle Model"
        readonly
        v-bind="attrs"
        v-on="on"
        color="#2e5bff"
    ></v-combobox>
    <p>Status</p>
    <v-combobox
        multiple
        label="Service needed"
        readonly
        v-bind="attrs"
        v-on="on"
        color="#2e5bff"
    ></v-combobox>
    <p>Location</p>
    <v-combobox
        multiple
        label="USA"
        readonly
        v-bind="attrs"
        v-on="on"
        color="#2e5bff"
    ></v-combobox>
  </v-card>
</template>

<script>
  export default {
    name: 'Lateral',
    data: () => ({
      width: 300,
      service: 14,
    }),
  }
</script>

<style scoped>

.pa-5{
  background-color: "#f4f6fc";
}

</style>