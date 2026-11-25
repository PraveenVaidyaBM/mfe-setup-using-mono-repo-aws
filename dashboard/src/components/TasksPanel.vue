<template>
  <div class="p-col-12 p-md-6 p-lg-4">
    <Panel header="Tasks" style="height: 100%">
      <ul class="task-list">
        <li v-for="task in tasks" :key="task.value">
          <Checkbox name="task" :value="task.value" v-model="selectedTasks" />
          <span class="task-name">{{ task.name }}</span>
          <i :class="task.icon" />
        </li>
      </ul>
    </Panel>
  </div>
</template>

<script>
import Checkbox from 'primevue/checkbox';
import Panel from 'primevue/panel';

export default {
  components: { Checkbox, Panel },
  data() {
    return {
      selectedTasks: [],
      tasks: [
        { name: 'Sales Reports', value: 'reports', icon: 'pi pi-chart-bar' },
        { name: 'Pay Invoices', value: 'invoices', icon: 'pi pi-dollar' },
        { name: 'Dinner with Tony', value: 'dinner', icon: 'pi pi-user' },
        { name: 'Client Meeting', value: 'meeting', icon: 'pi pi-users' },
        { name: 'New Theme', value: 'theme', icon: 'pi pi-globe' },
        { name: 'Flight Ticket', value: 'flight', icon: 'pi pi-briefcase' },
      ],
    };
  },
};
</script>
