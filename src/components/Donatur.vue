<template>
  <div>
    <div class="form-group">
      <label for="donatur">Donatur</label>
      <select
        @change="$emit('selected-donatur', $event.target.value)"
        class="form-control"
      >
        <option value="">Pilih Donatur</option>
        <option
          v-for="donatur in listDonatur"
          :key="donatur.id"
          :value="donatur.name"
        >
          {{ donatur.name }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  name: "Donatur",
  computed: {
    listDonatur() {
      return this.$store.state.donatur.listDonatur;
    },
  },
};
</script>

<style scoped></style>
