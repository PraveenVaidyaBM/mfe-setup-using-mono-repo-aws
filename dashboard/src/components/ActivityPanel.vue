<template>
  <div class="p-col-12 p-lg-4">
    <Panel header="Activity" style="height: 100%">
      <div class="activity-header">
        <div class="p-grid">
          <div class="p-col-6">
            <span style="font-weight: bold">Last Activity</span>
            <p>Updated 1 minute ago</p>
          </div>
          <div class="p-col-6" style="text-align: right">
            <Button label="Refresh" icon="pi pi-refresh" />
          </div>
        </div>
      </div>

      <ul class="activity-list">
        <li>
          <div class="p-d-flex p-jc-between p-ai-center p-mb-3">
            <h5 class="activity p-m-0">Income</h5>
            <div class="count">$900</div>
          </div>
          <ProgressBar :value="95" :showValue="false" />
        </li>
        <li>
          <div class="p-d-flex p-jc-between p-ai-center p-mb-3">
            <h5 class="activity p-m-0">Tax</h5>
            <div class="count" style="background-color: #f9c851">$250</div>
          </div>
          <ProgressBar :value="24" :showValue="false" />
        </li>
      </ul>
    </Panel>
  </div>
</template>

<script>
import Panel from 'primevue/panel';
import Button from 'primevue/button';
import ProgressBar from 'primevue/progressbar';

export default {
  components: { Panel, Button, ProgressBar },
};
</script>
