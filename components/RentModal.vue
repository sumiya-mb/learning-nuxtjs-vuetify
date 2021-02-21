<template>
  <div id="app" >
    <v-app>
      <div class="text-center">
        <v-dialog
          v-model="dialog"
          width="500"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="red lighten-2"
              dark
              v-bind="attrs"
              v-on="on"
            >
              Rent
            </v-btn>
          </template>

          <v-card>
            <v-card-title class="headline grey lighten-2">
              Order confirmation
            </v-card-title>
            <div class="calendar-container">
              <v-card-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
                dolore magna aliqua.
              </v-card-text>
              <vc-date-picker
                :value="null"
                color="indigo"
                is-dark
                is-range
              />
            </div>
            <v-divider></v-divider>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="primary"
                text
                @click="() => {
                  dialog = false
                  addItem(product.id)
                }"
              >
                Order
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </div>
    </v-app>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  data () {
    return {
      dialog: false
    }
  },
  props: ['product'],
  methods: {
    ...mapMutations(['addItem'])
  }
}
</script>

<style scoped>
#app{
  margin-top: 1rem;
  height: 5rem;
}

.v-application--is-ltr {
  background: none;
}

.v-sheet {
  background: white;
}

.v-card__title, .v-card__text {
  color: black !important;
}

.calendar-container{
  display: flex;
  padding: 1rem;
}

</style>
