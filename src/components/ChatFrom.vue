<template>
  <q-icon name="eva-upload-outline"></q-icon>
  <div class="form">
    <input
      class="form__input"
      type="text"
      placeholder="투표를 해야 의견을 남길 수 있어요!"
      v-model.trim="msg"
      @keyup.enter="submitMessage"
    />
    <div @click="submitMessage" class="form__submit">
      <svg
        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
        width="25"
        height="25" fill="#CCCCCC">
        <g data-name="Layer 2">
          <g data-name="paper-plane">
            <rect width="24" height="24" opacity="0"/>
            <path d="M21 4a1.31 1.31 0 0 0-.06-.27v-.09a1 1 0 0 0-.2-.3 1 1 0 0 0-.29-.19h-.09a.86.86 0 0 0-.31-.15H20a1 1 0 0 0-.3 0l-18 6a1 1 0 0 0 0 1.9l8.53 2.84 2.84 8.53a1 1 0 0 0 1.9 0l6-18A1 1 0 0 0 21 4zm-4.7 2.29l-5.57 5.57L5.16 10zM14 18.84l-1.86-5.57 5.57-5.57z"/>
          </g>
        </g>
      </svg>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    submitMessage () {
      if (this.msg) {
        alert(this.msg)
        this.$emit('submitMessage', this.msg)
        this.msg = ''
      }
    }
  }
}
</script>

<style scoped>
.form {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem;
  background: #ffffff;
  border-radius: 30px 30px 30px 30px;
  box-shadow: 0px -5px 30px rgba(0, 0, 0, 0.05);
}
.form__input {
  border: none;
  padding: 0.5rem 1.3rem 0.1rem 1.3rem;
  font-size: 13px;
  width: calc(100% - 60px);
}
.form__input:focus {
  outline: none;
}
.form__submit {
  width: 30px;
  display: flex;
  align-items: center;
  cursor: pointer;
}
svg {
  transition: 0.3s;
}
svg:hover {
  fill: #999999;
}
</style>
