<template>
  <div>
    <p>{{$route.params.species}}</p>
    <p>{{animal.name}}</p>
    <!-- {{pet().name}} -->
    <!-- {{$route.params.species}}
    {{$route.params.id}} -->
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data () {
    return {
      animal: {}
    }
  },
  computed: {
    ...mapState(['cats', 'dogs'])
  },
  // methods: {
  //   pet () {
  //     // this.cats this['cats']
  //     const animal = this[this.$route.params.species][this.$route.params.id]
  //     return animal
  //   }
  //  }
  mounted () {
    const animal = this[this.$route.params.species][this.$route.params.id]
    this.animal = animal
  }
}
</script>

<style scoped>
</style>
