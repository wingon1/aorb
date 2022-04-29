<template>
  <div class="q-pa-md">
    <div class="chat__mymessage">
      <div class="chat__mymessage__paragraph bg-amber-3">
        <p>{{ msg }}</p>
        <p class="name-date">{{ name }} | {{ date }}</p></div>
    </div>
    <div class="chat__yourmessage">
        <div class="chat__yourmessage__paragraph bg-green-3">
          <p>{{ msg }}</p>
          <p class="name-date">{{ name }} | {{ date }}</p>
        </div>
    </div>
    <div class="chat__mymessage">
      <div class="chat__mymessage__paragraph bg-amber-3">
        <p>ㅇㅇㅇ</p>
        <p class="name-date">{{ name }} | {{ date }}</p></div>
    </div>
  </div>
  <q-footer style="padding: 5px; background: #fafafa00">
    <ChatFrom/>
<!--    <q-input rounded dense outlined  v-model="text" bg-color="green-2" color="green-5">-->
<!--      <template v-slot:append>-->
<!--        <q-btn round dense flat icon="send" @click="isPwd = !isPwd"/>-->
<!--      </template>-->
<!--    </q-input>-->
  </q-footer>
</template>

<script>
import ChatFrom from 'components/ChatFrom'

export default {
  name: 'CommentComponent.vue',
  components: {
    ChatFrom
  },
  props: {
    msg: {
      type: String,
      default: '오늘 점심 뭐 먹을까용?늘 점심 뭐 먹을까용?늘 점심 뭐 먹을까용?늘 점심 뭐 먹을까용?ddd'
    },
    name: {
      type: String,
      default: '두더지'
    },
    date: {
      type: String,
      default: '2022.05.05'
    }
  }
}
</script>

<style>
.chat__mymessage {
  display: flex;
  justify-content: right;
  align-items: flex-end;
  margin: 0;
  min-height: 40px;
  line-break: anywhere;
}
.chat__mymessage__paragraph {
  margin: 0.4rem 0 0 1rem;
  border-radius: 20px 20px 0px 20px;
  max-width: 80%;
  min-width: 50%;
  background-color: #bbc4ef;
  color: #414141;
  padding: 0.8rem;
  font-size: 14px;
}
.chat__mymessage__paragraph p{
  padding: 0;
  margin: 0;
}
.chat__yourmessage {
  display: flex;
}
.chat__yourmessage__paragraph {
  margin: 0.4rem 1rem 0 0;
  border-radius: 20px 20px 20px 0px;
  background-color: #f3f3f3;
  max-width: 80%;
  color: #414141;
  padding: 0.8rem;
  font-size: 14px;
}
.chat__yourmessage__paragraph p{
  padding: 0;
  margin: 0;
}
.chat__mymessage__paragraph .name-date{
  font-size: 8px;
  color: rgba(65, 65, 65, 0.65);
  padding-top: 5px;
}
.chat__yourmessage__paragraph .name-date{
  font-size: 8px;
  color: rgba(65, 65, 65, 0.65);
  padding-top: 5px;
}
.chat__yourmessage__time {
  margin: 0;
  font-size: 12px;
  color: #9c9c9c;
}
</style>
