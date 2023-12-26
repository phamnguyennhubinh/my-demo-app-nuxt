<template>
  <div>
    <b-card header="Light table" header-tag="header" footer-tag="footer">
      <b-table-simple hover>
        <b-thead>
          <b-tr>
            <b-th>PROJECT</b-th>
            <b-th>BUDGET</b-th>
            <b-th>STATUS</b-th>
            <b-th>USERS</b-th>
            <b-th>COMPLETION</b-th>
          </b-tr>
        </b-thead>
        <b-tbody>
          <b-tr v-for="item in items" :key="item">
            <b-td>{{ item.project }}</b-td>
            <b-td>{{ item.budget }}</b-td>
            <b-td>{{ item.status }}</b-td>
            <b-td>{{ item.users }}</b-td>
            <b-td>{{ item.completion }}</b-td>
          </b-tr>
        </b-tbody>
      </b-table-simple>
      <template #footer>
        <b-pagination class="d-flex justify-content-end"
          v-model="currentPage"
          pills
          :total-rows="rows"
        ></b-pagination>
      </template>
    </b-card>
  </div>
</template>

<script>
import items from "../assets/components/LightTable/main";

export default {
  props: {items},
  data() {
    return {
      rows: 100,
      currentPage: 1,
    };
  },
};
</script>

<style scoped src="../assets/components/LightTable/main.css"></style>
