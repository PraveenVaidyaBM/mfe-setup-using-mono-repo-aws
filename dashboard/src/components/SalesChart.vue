<template>
  <div class="p-col-12 p-lg-6">
    <div class="card">
      <Chart type="line" :data="data" />
    </div>
  </div>
</template>

<script>
import Chart from 'primevue/chart';

export default {
  components: { Chart },
  props: {
    data: {
      type: Object,
      required: true,
    },
  },
};
</script>
