<template>
	<div>
		<input v-model="login" type="text" placeholder="Login">
		<input v-model="password" type="password" placeholder="Pass">
		<input type="submit" placeholder="Join" v-on:clock="submit">
	</div>
</template>
<script type="text/javascript">
	import axios from 'axios'

	export default{
		data(){
			return{
				login: '',
				password: '',

			}

		},
		methods: {
			axios.get('http://37.77.104.246/api/jsonstorage/?id=642d1ca9c540df262dcdd1df3f445cd5')
				.then(res) =>{
					let result = false;
					let user;
					{for(let i = 0; i<res.data.length; i++){
						
						if( this.login == res.data[i].login && this.password == res.data[i].password){
							result = true;

						}
					}
				}
					
				

		


</script>
