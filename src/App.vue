<template>
<div>
<login-form @login="logMeIn($event)"></login-form>
</div>
</template>
<script>
import LoginForm from "./LoginForm";
export default{
	components: {LoginForm}
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
