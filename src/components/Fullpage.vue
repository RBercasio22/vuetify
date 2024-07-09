<template>
    <div class="text-center">
      <v-btn
        :disabled="loading"
        append-icon="mdi-refresh"
        text="Refresh"
        variant="outlined"
        @click="onClick"
      ></v-btn>
    </div>
  
    <v-data-table :items="items" :loading="loading">
      <template v-slot:loading>
        <v-skeleton-loader type="table-row@10"></v-skeleton-loader>
      </template>
    </v-data-table>
  </template>
  <script>
    import { shallowRef } from 'vue'
  
    export default {
      data () {
        return {
          loading: false,
          items: [
            { name: 'Chevrolet Camaro', year: 1967, engine: 'V8', horsepower: 375, torque: 415 },
            { name: 'Ford Mustang', year: 1965, engine: 'V8', horsepower: 271, torque: 312 },
            { name: 'Dodge Charger', year: 1968, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'Pontiac GTO', year: 1964, engine: 'V8', horsepower: 350, torque: 445 },
            { name: 'Plymouth Barracuda', year: 1964, engine: 'V8', horsepower: 330, torque: 425 },
            { name: 'Chevrolet Chevelle SS', year: 1970, engine: 'V8', horsepower: 450, torque: 500 },
            { name: 'Oldsmobile 442', year: 1971, engine: 'V8', horsepower: 340, torque: 440 },
            { name: 'Dodge Challenger', year: 1970, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'AMC Javelin', year: 1968, engine: 'V8', horsepower: 315, torque: 425 },
            { name: 'Mercury Cougar', year: 1967, engine: 'V8', horsepower: 335, torque: 427 },
            { name: 'Chevrolet Corvette', year: 1969, engine: 'V8', horsepower: 350, torque: 360 },
            { name: 'Ford Torino', year: 1970, engine: 'V8', horsepower: 375, torque: 450 },
            { name: 'Pontiac Firebird', year: 1969, engine: 'V8', horsepower: 325, torque: 410 },
            { name: 'Buick Skylark GSX', year: 1970, engine: 'V8', horsepower: 360, torque: 510 },
            { name: 'Plymouth Road Runner', year: 1969, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'Chevrolet Nova SS', year: 1968, engine: 'V8', horsepower: 375, torque: 415 },
            { name: 'Oldsmobile Cutlass', year: 1972, engine: 'V8', horsepower: 300, torque: 380 },
            { name: 'Dodge Super Bee', year: 1970, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'AMC Rebel', year: 1969, engine: 'V8', horsepower: 340, torque: 430 },
            { name: 'Mercury Cyclone', year: 1968, engine: 'V8', horsepower: 325, torque: 425 },
            { name: 'Chevrolet Corvette', year: 1969, engine: 'V8', horsepower: 350, torque: 360 },
            { name: 'Ford Torino', year: 1970, engine: 'V8', horsepower: 375, torque: 450 },
            { name: 'Pontiac Firebird', year: 1969, engine: 'V8', horsepower: 325, torque: 410 },
            { name: 'Buick Skylark GSX', year: 1970, engine: 'V8', horsepower: 360, torque: 510 },
            { name: 'Plymouth Road Runner', year: 1969, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'Chevrolet Nova SS', year: 1968, engine: 'V8', horsepower: 375, torque: 415 },
            { name: 'Oldsmobile Cutlass', year: 1972, engine: 'V8', horsepower: 300, torque: 380 },
            { name: 'Dodge Super Bee', year: 1970, engine: 'V8', horsepower: 425, torque: 490 },
            { name: 'AMC Rebel', year: 1969, engine: 'V8', horsepower: 340, torque: 430 },
            { name: 'Mercury Cyclone', year: 1968, engine: 'V8', horsepower: 325, torque: 425 }

          ],
        }
      },
      methods: {
        onClick () {
          this.loading = true
          setTimeout(() => {
            this.loading = false
          }, 10000)
        },
      },
    }
  </script>