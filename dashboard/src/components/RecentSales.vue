<template>
  <div class="p-col-12 p-lg-6">
    <div class="card">
      <h1 style="font-size: 16px">Recent Sales</h1>
      <DataTable
        :value="products"
        class="p-datatable-customers"
        :rows="5"
        style="margin-bottom: 20px"
        :paginator="true"
      >
        <Column>
          <template #header> Logo </template>
          <template #body="slotProps">
            <img
              :src="'assets/layout/images/product/' + slotProps.data.image"
              :alt="slotProps.data.image"
              width="50"
            />
          </template>
        </Column>
        <Column field="name" header="Name" :sortable="true"></Column>
        <Column field="category" header="Category" :sortable="true"></Column>
        <Column field="price" header="Price" :sortable="true">
          <template #body="slotProps">
            {{ formatCurrency(slotProps.data.price) }}
          </template>
        </Column>
        <Column>
          <template #header> View </template>
          <template #body>
            <Button
              icon="pi pi-search"
              type="button"
              class="p-button-success p-mr-2 p-mb-1"
            ></Button>
            <Button
              icon="pi pi-times"
              type="button"
              class="p-button-danger p-mb-1"
            ></Button>
          </template>
        </Column>
      </DataTable>
    </div>
  </div>
</template>

<script>
import Column from 'primevue/column';
import DataTable from 'primevue/datatable';
import Button from 'primevue/button';

export default {
  components: { Column, DataTable, Button },
  props: {
    products: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    formatCurrency(value) {
      return value.toLocaleString('en-US', {
        style: 'currency',
        currency: 'USD',
      });
    },
  },
};
</script>
