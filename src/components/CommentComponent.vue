<template>
  <div class="q-pa-md">
    <div class="chat__mymessage">
      <div class="chat__mymessage__paragraph bg-amber-3">
        <span class="name">{{ name }}</span>
        <p>{{ msg }}</p>
        <div class="name-date">
          <div class="inline-block">
            <svg xmlns="http://www.w3.org/2000/svg" width="10" height="10" fill="rgba(65, 65, 65, 0.65)" viewBox="0 0 24 16">
              <g data-name="Layer 2">
                <g data-name="heart">
                  <rect width="10" height="10" opacity="0"/>
                  <path d="M12 21a1 1 0 0 1-.71-.29l-7.77-7.78a5.26 5.26 0 0 1 0-7.4 5.24 5.24 0 0 1 7.4 0L12 6.61l1.08-1.08a5.24 5.24 0 0 1 7.4 0 5.26 5.26 0 0 1 0 7.4l-7.77 7.78A1 1 0 0 1 12 21zM7.22 6a3.2 3.2 0 0 0-2.28.94 3.24 3.24 0 0 0 0 4.57L12 18.58l7.06-7.07a3.24 3.24 0 0 0 0-4.57 3.32 3.32 0 0 0-4.56 0l-1.79 1.8a1 1 0 0 1-1.42 0L9.5 6.94A3.2 3.2 0 0 0 7.22 6z"/>
                </g>
              </g>
            </svg>
            조아용 {{ like }}
          </div>
          <p class="inline-block" style="float: right;"> {{ date }}</p>
        </div>
      </div>
    </div>
    <div class="chat__yourmessage">
        <div class="chat__yourmessage__paragraph bg-green-3">
          <span class="name">{{ name }}</span>
          <p>{{ msg }}</p>
          <div class="name-date">
            <div class="inline-block">
              <svg xmlns="http://www.w3.org/2000/svg" width="10" height="10" fill="rgba(65, 65, 65, 0.65)" viewBox="0 0 24 16">
                <g data-name="Layer 2">
                  <g data-name="heart">
                    <rect width="10" height="10" opacity="0"/>
                    <path d="M12 21a1 1 0 0 1-.71-.29l-7.77-7.78a5.26 5.26 0 0 1 0-7.4 5.24 5.24 0 0 1 7.4 0L12 6.61l1.08-1.08a5.24 5.24 0 0 1 7.4 0 5.26 5.26 0 0 1 0 7.4l-7.77 7.78A1 1 0 0 1 12 21zM7.22 6a3.2 3.2 0 0 0-2.28.94 3.24 3.24 0 0 0 0 4.57L12 18.58l7.06-7.07a3.24 3.24 0 0 0 0-4.57 3.32 3.32 0 0 0-4.56 0l-1.79 1.8a1 1 0 0 1-1.42 0L9.5 6.94A3.2 3.2 0 0 0 7.22 6z"/>
                  </g>
                </g>
              </svg>
              조아용 {{ like }}
            </div>
            <p class="inline-block" style="float: right;"> {{ date }}</p>
          </div>
        </div>
    </div>
    <div class="chat__mymessage">
      <div class="chat__mymessage__paragraph bg-amber-3">
        <span class="name">{{ name }}</span>
        <p>ㅇㅇㅇ</p>
        <div class="name-date">
          <div class="inline-block">
            <svg xmlns="http://www.w3.org/2000/svg" width="10" height="10" fill="rgba(65, 65, 65, 0.65)" viewBox="0 0 24 16">
              <g data-name="Layer 2">
                <g data-name="heart">
                  <rect width="10" height="10" opacity="0"/>
                  <path d="M12 21a1 1 0 0 1-.71-.29l-7.77-7.78a5.26 5.26 0 0 1 0-7.4 5.24 5.24 0 0 1 7.4 0L12 6.61l1.08-1.08a5.24 5.24 0 0 1 7.4 0 5.26 5.26 0 0 1 0 7.4l-7.77 7.78A1 1 0 0 1 12 21zM7.22 6a3.2 3.2 0 0 0-2.28.94 3.24 3.24 0 0 0 0 4.57L12 18.58l7.06-7.07a3.24 3.24 0 0 0 0-4.57 3.32 3.32 0 0 0-4.56 0l-1.79 1.8a1 1 0 0 1-1.42 0L9.5 6.94A3.2 3.2 0 0 0 7.22 6z"/>
                </g>
              </g>
            </svg>
            조아용 {{ like }}
          </div>
          <p class="inline-block" style="float: right;"> {{ date }}</p>
        </div>
      </div>
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
    },
    like: {
      type: Number,
      default: 1
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
.name {
  font-size: 10px;
  font-weight: bold;
  color: rgba(65, 65, 65, 0.65);
  display: block;
  margin-bottom: 4px;
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
