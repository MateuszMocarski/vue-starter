<template>
<div id="app">
<div v-if="!logged"><login-form @login="checkEmailAndLogIn($event)" :button-label="'Log in'"></login-form></div>

	
</div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";

export default {
	data() {
		  return {
		    email: '',
		    password: '',
		    logged: false
		    };
		},
	components: {LoginForm},
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
