<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    />
    <div>
      <h5 class="text-size-21 q-mt-none q-mb-md">Text</h5>
      <div>
        <p class="text-bold">
          <span class="text-primary text-size-16 q-ma-sm">Primary</span>
          <span class="text-secondary text-size-16 q-ma-sm">Secondary</span>
          <span class="text-positive text-size-16 q-ma-sm">Positive</span>
          <span class="text-negative text-size-16 q-ma-sm">Negative</span>
        </p>
      </div>
    </div>
    <div class="div">
      <p class="text-bold">
        <span class="text-dark text-size-16 q-ma-sm">Dark</span>
        <span class="text-medium text-size-16 q-ma-sm">Medium</span>
        <span class="text-light text-size-16 q-ma-sm">Light</span>
      </p>
    </div>

    <q-separator class="q-my-md" />

    <!-- forms -->
    <h5 class="text-size-21 q-mt-none q-mb-md">Forms</h5>
    <div class="q-mb-md">
      <q-checkbox
        v-model="forms.checkbox"
        class="text-size-16"
        color="primary"
        label="Label on Left"
        left-label
      />
    </div>
    <div class="q-mb-md">
      <q-radio
        v-model="forms.radio"
        class="text-size-16"
        color="primary"
        label="line"
      />
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
});
</script>
