<template>
  <div>
    <div class="form-group">
      <label for="jenis_bantuan">Jenis Bantuan</label>
      <select
        @change="$emit('selected-bantuan', $event.target.value)"
        class="form-control"
      >
        <option value="">Pilih Bantuan</option>
        <option
          v-for="bantuan in listBantuan"
          :key="bantuan.id"
          :value="bantuan.name"
        >
          {{ bantuan.name }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  name: "clients",
  computed: {
    listBantuan() {
      return this.$store.state.clients.listBantuan;
    },
  },
};
</script>

<style scoped></style>
