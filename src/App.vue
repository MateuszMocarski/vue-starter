<template>
<div id="app">
	<h1>Welcome to signing system</h1>
	<div v-if="logged==false">
		<p>Email:</p>
		<input type="email" v-model="email">
		<p>Password:</p>
		<input type="password" v-model="password">
		<br></br>
		<div v-if="email.length > 0 && password.length > 0 && validEmail(email)">
			<button @click="logged=true">Zaloguj</button>
		</div>	
	</div>
	<div v-else>
		<p>Witaj {{email}}</p>
		<br></br>
		<button @click="logout()">Wyloguj</button>
	</div>
	
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
	data() {
		  return {
		    email: '',
		    password: '',
		    logged: false
		    };
		},
		methods: {
			  alertMyEmail() {
			    alert(this.email);
			  },
			  logout(){
				  this.email = '',
				  this.password = '',
				  this.logged = false
			  },
			  validEmail: function (email) {
			      var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
			      return re.test(email);
			    }
			}
}
</script>

<style>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
