<template>
    <table/>
</template>>

<script>
export default {
    var demo = new Vue({
	el: "#app",
	data: {
		newSpec: {
			title: "",
			value: ""
		},
		specs: [
			{
				title: "Name",
				value: ""
			},
			{
				title: "Room No",
				value: "12\""
			},
			{
				title: "ID PHOTO",
				value: "16\""
			},
			{
				title: "CHeck In",
				value: "20\""
			},
			{
				title: "Check Out",
				value: "71 lbs"
			}
		]
	},
	methods: {
    addSpec: function (e) {
			// alert('add me');
			e.preventDefault();
			if (this.newSpec.title == '') return;
      this.specs.push({
        title: this.newSpec.title,
        value: this.newSpec.value
      });
      this.newSpec.title = this.newSpec.value = '';
			this.$refs.title.focus();
		},
    removeSpec: function (index) {
			this.specs.splice(index,1);
    },
		moveSpecUp: function (index) {
			this.specs.splice( (index-1), 0, this.specs.splice(index,1)[0] );
		},
		moveSpecDown: function (index) {
			this.specs.splice( (index+1), 0, this.specs.splice(index,1)[0] );
		}
  }
});
</script>>