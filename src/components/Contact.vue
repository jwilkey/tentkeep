<template>
  <div class="contact">
    <titlebar></titlebar>

    <div class="pad">
      <div class="theme-mid pad rounded shadow marginb">
        <h1>Contact Tentkeep</h1>
        <p class="marginb">Please use the form below to contact our representatives, and we will get back to you promptly.</p>

        <br />
        <div v-if="messageSent" class="marginb">
          <p>Thank You! Your message has been sent.</p>
          <router-link to="/" class="callout alt">Return to home page</router-link>
        </div>
        <div class="flex-column">
          <div id="content" @click="startTyping" @blur="stopEditing" contenteditable="true" class="shadow-inset pad marginb rounded">
            <p v-if="!editing && !content" class="muted">type your request or questions here...</p>
          </div>
        </div>
        <div class="flex-row marginb">
          <div class="flex-one"></div>
          <button @click="send">SEND</button>
        </div>
        <br />

        <div class="hi-bottom marginb"></div>

        <p class="marginb">Thank you for your interest in working with Tentkeep. The products we create are sure to impress you as well as your audience. We will help you discover and build the perfect solution for your needs.</p>
      </div>
    </div>
  </div>
</template>

<script>
import Titlebar from '@/components/Titlebar'

export default {
  name: 'contact',
  data () {
    return {
      editing: false,
      content: '',
      messageSent: false
    }
  },
  components: { Titlebar },
  methods: {
    startTyping () {
      this.editing = true
    },
    stopEditing () {
      this.content = this.$el.querySelector('#content').textContent
      this.editing = false
    },
    send () {
      const url = 'https://tentkeep.herokuapp.com/mail'
      const data = {
        subject: 'Consultation Request',
        content: this.content
      }

      fetch(url, {
        method: 'POST',
        body: JSON.stringify(data),
        headers: new Headers({ 'Content-Type': 'application/json' })
      })

      this.messageSent = true
      this.$el.querySelector('#content').textContent = ''
      this.content = ''
      this.editing = false
    }
  }
}
</script>

<style lang="less" scoped>
.contact {
  h1 {
    margin: 0;
    margin-bottom: 10px;
  }
  #content {
    min-height: 100px;
  }
}
</style>
