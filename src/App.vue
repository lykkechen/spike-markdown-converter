<template>
  <div id="app">
    <div 
      v-html="html">
    </div>
  </div>
</template>

<script>
  import marked from 'marked'

export default {
  name: 'app',
  data () {
    return {
      markdown: ``,
      html: ''
    }
  },
  created() {
    this.transform(this.markdown)
  },
  methods: {
     transform: function (markdown) {
      this.html = marked(markdown, { sanitize: true })
      console.log(this.html)
    }
  }
}
</script>

<style>
</style>
