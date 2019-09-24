<template>
	<table>
		<tr v-for="guest in guests" :key="guest.room">
			<td>{{ guest.name }}</td>
			<td>{{ guest.room }}</td>
		</tr>
	</table>
</template>

<script>
export default {
	props: ['guests']
};
</script>