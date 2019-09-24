<template>
	<div class="home center">
		<camera />
		<table-o :guests="guests" />
	</div>
</template>

<script>
// @ is an alias to /src
import Camera from "@/components/Camera.vue";
import TableO from "@/components/TableO.vue";

export default {
	name: "home",
	components: {
		Camera,
		TableO
	},
	data() {
		return {
			guests: []
		};
	},
	methods:{
		fetchGusts(){

			let temp =[
				{
					name: "krushn",
					room: 23
				},
				{
					name: "tushar",
					room: 24
				},
				{
					name: "adrak",
					room: 25
				}
			]

			this.guests = temp
		}
	},
	mounted(){
		this.fetchGusts()
	}
};
</script>
