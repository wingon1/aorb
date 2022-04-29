<template>
  <div class="q-pa-md">
    <q-card class="my-card" flat bordered>
      <q-item>
<!--        <q-item-section avatar>-->
<!--          <q-avatar>-->
<!--            <q-icon size="md" name="face" color="grey-5"></q-icon>-->
<!--          </q-avatar>-->
<!--        </q-item-section>-->
        <q-item-section>
          <q-item-label>{{ title }}</q-item-label>
          <q-item-label caption>
            {{ name }}
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator></q-separator>

      <q-card-section horizontal>
        <q-btn flat style="padding-bottom: 20px; padding-top: 20px;" class="col" :ripple="{ color: 'green-3' }" color="grey-9" :label="item1"></q-btn>
        <q-separator vertical></q-separator>
        <q-btn flat style="padding-bottom: 20px; padding-top: 20px;" class="col" :ripple="{ color: 'amber-3' }" color="grey-9" :label="item2"></q-btn>
      </q-card-section>
      <q-linear-progress :value="progress" track-color="amber-3" color="green-3"></q-linear-progress>
      <q-card-actions>
        <q-item-label style="margin-left: 10px; color: #424242" class="text-overline">25명이 투표했어요!</q-item-label>
        <q-space></q-space>
        <q-btn :ripple="false" flat round color="grey-5" style="font-size: 0.8em;" icon="gavel"></q-btn>
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CardComponent',
  props: {
    title: {
      type: String,
      default: '오늘 점심 뭐 먹을까용?🧡🧑'
    },
    item1: {
      type: String,
      default: '🧡대충 머근다🧡'
    },
    item2: {
      type: String,
      default: '🧡으으 시켜머근다🧡🧡🧡🧡🧡'
    },
    name: {
      type: String,
      default: '익명'
    },
    progress: {
      type: Number,
      default: 0.2
    }
  }
})
</script>
