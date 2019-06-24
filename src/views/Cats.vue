<template>
  <div>
    <PetTable species="cats" :pets="cats" />
    <!-- <b-table striped hover :items="cats">
      <template slot="name" slot-scope="data">
        <router-link :to="`/pets/cats/${data.index}`" >
          {{data.value}}
        </router-link>
      </template>
    </b-table> -->
  </div>
</template>

<script>
// import cats from '@/data/cats'
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
    ...mapState(['cats'])
  }
}
</script>

<style scoped>
</style>
