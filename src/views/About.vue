<template>
  <div class="about">
    <h1>This is an about page</h1>
    <input v-model="message" />
    <button @click="click">点击一下试试</button>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import { io } from 'socket.io-client'

export default defineComponent({
  props: {},
  data () {
    return { message: '', socket: null}
  },
  mounted () {
    this.socket = io('ws://127.0.0.1:2333')
    this.socket.on('receiveMsg', (connectMsg) => {
      console.log(connectMsg)
    })
  },
  methods: {
    click () {
      console.log('aaa clicked')
      this.socket.emit('startSendMsg', this.message)
    }
  }

})
</script>
