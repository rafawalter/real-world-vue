<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <p>This event is created by {{ user.name }}</p>
    <p>{{ getEvent(1) }}</p>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength
    },
    getEvent() {
      return this.$store.getters.getEventById
    },
    ...mapGetters({
      catCount: 'categoriesLength',
      getEvent: 'getEventById'
    }),
    ...mapState(['categories', 'user'])
  }
}
</script>

<style scoped></style>
