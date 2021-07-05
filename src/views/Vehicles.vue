<template>
  
  <v-container fluid class="aber">
    <v-layout row wrap class="pa-5">
      <v-flex xs12 md9 class="pa-5">
        <barra-dash />
        <v-data-table
            :headers="headers"
            :items="vehicles"
            :items-per-page="8"
            class="elevation-1">
        </v-data-table>
      </v-flex>
      <v-flex xs12 md3 class="pa-7">
        <lateral />
        <div class="text-right pt-7">
          <v-btn
            class="mx-2"
            fab
            color="#2e5bff"
            
          >
            <v-icon color="white" large>
              mdi-plus
            </v-icon>
          </v-btn>
        </div>
        
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  import BarraDash from '../components/BarraDash.vue'
  import Lateral from '../components/Lateral.vue'


  export default {
  components: { BarraDash, Lateral },
    data () {
      return {
        
        headers: [
          {
            text: 'NAME AND ID',
            align: 'start',
            sortable: true,
            value: 'name',
          },
          { text: 'VEHICLE MODEL', value: 'model', sortable: false },
          { text: 'NEXT SERVICE', value: 'service', sortable: false },
          { text: 'TRIPS', value: 'trips', sortable: false },
          { text: 'ENERGY USED', value: 'energy', sortable: false },
          { text: '', value: 'manage', sortable: false },
        ],
        vehicles: [
          {
            name: 'Spire',
            id: '#12010',
            model: 'Tesla Model X',
            service: '08/21/2018',
            trips: 774,
            energy: '450 kWh',
            manage: 'manage',
          },
          {
            name: 'Eos',
            id: '#12011',
            model: 'Volvo Intellisafe',
            service: '06/12/2018',
            trips: 825,
            energy: '321 kWh',
            manage: 'manage',
          },
          {
            name: 'Eagle',
            id: '#12012',
            model: 'BMW 7 Series',
            service: '06/16/2018',
            trips: 125,
            energy: '230 kWh',
            manage: 'manage',
          },
          {
            name: 'Expedition',
            id: '#12013',
            model: 'Infiniti Q50S',
            service: '07/02/2018',
            trips: 734,
            energy: '129 kWh',
            manage: 'manage',
          },
          {
            name: 'Bliss',
            id: '#12014',
            model: 'Audi RS 7',
            service: '08/27/2018',
            trips: 823,
            energy: '553 kWh',
            manage: 'manage',
          },
          {
            name: 'Vigor',
            id: '#12015',
            model: 'Tesla Model S',
            service: '10/02/2018',
            trips: 1142,
            energy: '650 kWh',
            manage: 'manage',
          },
        ],
      }
    },
  }
</script>

