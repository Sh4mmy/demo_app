<template>
    <div class="flex h-screen flex-col overflow-hidden p-5">
  <Calendar
    :config="{
      defaultMode: 'Month',
      isEditMode: true,
      eventIcons: {
      },
      allowCustomClickEvents: true,
      redundantCellHeight: 100,
      enableShortcuts: true,
    }"
    :events="[
      
    ]"
    :create="(event) => logEvent('createEvent', event)"
    :update="(event) => logEvent('updateEvent', event)"
    :delete="(event) => logEvent('deleteEvent', event)"
  />
</div>
</template>
<script setup>
import { Calendar } from 'frappe-ui';

import { createListResource } from 'frappe-ui'
const eventList = createListResource({
  doctype: 'Event',
  fields: ['subject'],
  
})
todos.fetch()
</script>