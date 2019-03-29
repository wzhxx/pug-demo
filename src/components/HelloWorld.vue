<template lang="pug">

	div.hello
		h1 {{msg}}
		p For a guide and recipes on how to configure | customize this project,check out the
			a(href="https://cli.vuejs.org" target="_blank" rel="noopener") vue-cli documentation
		h3 Installed CLI plugins
		ul: li
			a(href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener") babel
			a(href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener") eslint
		h3 Essential Links
			ul: li(v-for="item in essentialLink"): a(:href="item.url" target="_blank" rel="noopener") {{item.name}}
		h3 Ecosystem
			ul
				li(v-for="item in ecosystem"): a(:href="item.url" target="_blank" rel="noopener") {{item.name}}
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
	data(){
		return{
			essentialLink: [{url:'https://vuejs.org',name: 'Core Docs'},{url:'https://chat.vuejs.org',name: 'Community Chat'},{url:'https://twitter.com/vuejs',name: 'Twiter'},{url:'https://news.vuejs.org',name: 'News'}],
			ecosystem:	[{url:'https://router.vuejs.org',name:'vue-router'},{url:'https://vuex.vuejs.org',name:'vuex'},{url:'https://github.com/vuejs/vue-devtools#vue-devtools',name: 'vue devtools'},{url:'https://vue-loader.vuejs.org',name:'vue-loader'},{url:'https://github.com/vuejs/awesome-vue',name:'awesome-vue'}]
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
