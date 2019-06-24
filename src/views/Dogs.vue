<template>
  <div>
        <PetTable species="dogs" :pets="dogs" />
    <!-- <h1>Dogs</h1>
    <b-table striped hover :items="dogs">
        <template slot="name" slot-scope="data">
          <router-link :to="`/pets/dogs/${data.index}`" >
            {{data.value}}
          </router-link>
        </template>
    </b-table> -->
  </div>
</template>

<script>
// import dogs from '@/data/dogs'
import { mapState } from 'vuex'
import PetTable from '@/components/PetTable.vue'

export default {
  components: {
    PetTable
  },
  data () {
    return {
    }
  },
  computed: {
    ...mapState(['dogs'])
  }
}
</script>

<style scoped>
</style>
