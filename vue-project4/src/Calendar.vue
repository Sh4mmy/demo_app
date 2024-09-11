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
      {
        title: 'English by Ryan Mathew',
        participant: 'Ryan Mathew',
        id: 'EDU-CSH-2024-00091',
        venue: 'CNF-ROOM-2024-00001',
        fromDate: '2024-07-08 16:30:00',
        toDate: '2024-07-08 17:30:00',
        color: 'green',
      },
      {
        title: 'English by Ryan Mathew',
        participant: 'Ryan Mathew',
        id: 'EDU-CSH-2024-00092',
        venue: 'CNF-ROOM-2024-00002',
        fromDate: '2024-07-08 13:30:00',
        toDate: '2024-07-08 17:30:00',
        color: 'green',
      },
      {
        title: 'English by Sheldon',
        participant: 'Sheldon',
        id: 'EDU-CSH-2024-00093',
        venue: 'CNF-ROOM-2024-00001',
        fromDate: '2024-07-09 10:30:00',
        toDate: '2024-07-09 11:30:00',
        color: 'green',
      },
      {
        title: 'English by Ryan Mathew',
        participant: 'Ryan Mathew',
        id: 'EDU-CSH-2024-00094',
        venue: 'CNF-ROOM-2024-00001',
        fromDate: '2024-07-17 16:30:00',
        toDate: '2024-07-17 17:30:00',
        color: 'green',
      },
      {
        title: 'Google Meet with John ',
        participant: 'John',
        id: '#htrht41',
        venue: 'Google Meet',
        fromDate: '2024-07-21 00:00:00',
        toDate: '2024-07-21 23:59:59',
        color: 'amber',
        isFullDay: true,
      },
      {
        title: 'Zoom Meet with Sheldon',
        participant: 'Sheldon',
        id: '#htrht42',
        venue: 'Google Meet',
        fromDate: '2024-07-21 00:00:00',
        toDate: '2024-07-21 23:59:59',
        color: 'amber',
        isFullDay: true,
      },
    ]"
    :create="(event) => logEvent('createEvent', event)"
    :update="(event) => logEvent('updateEvent', event)"
    :delete="(event) => logEvent('deleteEvent', event)"
  />
</div>
</template>
<script setup>
import { Calendar } from 'frappe-ui';
</script>