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
        <q-chip size="xs">
          밸런스게임
        </q-chip>
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
        <div @click="submitMessage" class="form__submit">
          <svg
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 19"
            width="25"
            height="25" fill="#CCCCCC">
           <g data-name="Layer 2"><g data-name="message-circle"><circle cx="12" cy="12" r="1"/><circle cx="16" cy="12" r="1"/><circle cx="8" cy="12" r="1"/><path d="M19.07 4.93a10 10 0 0 0-16.28 11 1.06 1.06 0 0 1 .09.64L2 20.8a1 1 0 0 0 .27.91A1 1 0 0 0 3 22h.2l4.28-.86a1.26 1.26 0 0 1 .64.09 10 10 0 0 0 11-16.28zm.83 8.36a8 8 0 0 1-11 6.08 3.26 3.26 0 0 0-1.25-.26 3.43 3.43 0 0 0-.56.05l-2.82.57.57-2.82a3.09 3.09 0 0 0-.21-1.81 8 8 0 0 1 6.08-11 8 8 0 0 1 9.19 9.19z"/><rect width="24" height="24" opacity="0"/></g></g>
          </svg>
        </div>
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
