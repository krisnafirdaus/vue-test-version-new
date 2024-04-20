<script setup>
import { ref } from 'vue'

const msg = ref('Hello Mappirefng')
const todos = ref([])
const newTodo = ref('')

const handleClick = () => {
	msg.value = 'Hello Change'
	console.log(msg.value)
}

const AddTodo = () => {
	todos.value.push({
		id: Date.now(),
		text: 'New Todo'
	})
}

const data = [
	{
		id: 1, 
		name: 'John Doe',
		age: 30,
	},
	{
		id: 2,
		name: 'Andi',
		age: 20,
	}
]

</script>

<template>
	<div class="mapping" @click="handleClick">Hello Mapping</div>
	<ul>
		<li v-for="item in data" :key="item.id">
			{{ item.name }} - {{ item.age }}
		</li>
	</ul>
</template>

<style scoped>
 .mapping {
	color: red;
 }
</style>