<template>
  <div>
    <div class="table-responsive">
      <table class="table table-hover table-bordered">
        <thead>
          <tr>
            <th>#</th>
            <th>Donatur</th>
            <th>Jenis Bantuan</th>
            <th>Jumlah</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(row, index) in listTransaksi" :key="index">
            <td>{{ index + 1 }}</td>
            <td>{{ row.donatur }}</td>
            <td>{{ row.bantuan }}</td>
            <td>{{ row.jumlah }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "Transaksi",
  computed: {
    ...mapState("transaksi", {
      listTransaksi: (state) => state.listTransaksi,
    }),
  },
};
</script>

<style lang="less" scoped></style>
