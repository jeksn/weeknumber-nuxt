<script setup>

import { ref } from 'vue'
import dayjs from 'dayjs'
import weekYear from 'dayjs/plugin/weekOfYear'


const localeObject = {
    name: 'locale-settings',
    weekStart: 1,
    weekStartsOn: 1
}

dayjs.locale('locale-settings', localeObject);
dayjs.extend(weekYear)

const WeekNumber = ref(dayjs().week())

</script>
<template>
    <div class="flex items-center justify-center h-screen">
        <h2 class="animate-pulse text-[12rem] md:text-[20rem] text-white font-array">{{ WeekNumber }}</h2>
    </div>
</template>