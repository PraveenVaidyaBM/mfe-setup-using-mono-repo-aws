<template>
  <div class="p-col-12 p-md-6 p-lg-4 p-fluid contact-form">
    <Panel header="Contact Us">
      <div class="p-grid">
        <div class="p-col-12">
          <Dropdown
            v-model="city"
            :options="cities"
            optionLabel="name"
            placeholder="Select a City"
          />
        </div>
        <div class="p-col-12"><InputText type="text" placeholder="Name" /></div>
        <div class="p-col-12"><InputText type="text" placeholder="Age" /></div>
        <div class="p-col-12"><InputText type="text" placeholder="Message" /></div>
        <div class="p-col-12">
          <Button type="button" label="Send" icon="pi pi-envelope" />
        </div>
      </div>
    </Panel>
  </div>
</template>

<script>
import Panel from 'primevue/panel';
import Dropdown from 'primevue/dropdown';
import InputText from 'primevue/inputtext';
import Button from 'primevue/button';

export default {
  components: { Panel, Dropdown, InputText, Button },
  data() {
    return {
      city: null,
      cities: [
        { name: 'New York', code: 'NY' },
        { name: 'Rome', code: 'RM' },
        { name: 'London', code: 'LDN' },
        { name: 'Istanbul', code: 'IST' },
        { name: 'Paris', code: 'PRS' },
      ],
    };
  },
};
</script>
