<template>
	<div id="app">
		<Loading>
			<h1>Loading Content</h1>
			<div class="loading-item" :style="`width: 60%;`"></div>
			<div class="loading-item" :style="`width: 70%;`"></div>
			<div class="loading-item" :style="`width: 80%;`"></div>

			<h1>Loading Content with Image</h1>
			<div class="loading-item" style="width: 100px; height: 100px"></div>
			<div class="loading-item" :style="`width: 60%;`"></div>
			<div class="loading-item" :style="`width: 70%;`"></div>
			<div class="loading-item" :style="`width: 80%;`"></div>

			<h1>Loading Table</h1>
			<table>
				<thead>
					<tr>
						<th>Header 1</th>
						<th>Header 1</th>
						<th>Header 1</th>
						<th>Header 1</th>
						<th>Header 1</th>
						<th>Header 1</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
					</tr>
					<tr>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
						<td>
							<div class="loading-item"></div>
						</td>
					</tr>
				</tbody>
			</table>

			<h1>Loading with Status</h1>
			<button class="btn" @click="handleLoading()">Change status</button>
			<div v-if="isLoading" class="loading-item"></div>
			<div v-if="!isLoading">
				Occaecat duis reprehenderit eu culpa consequat amet dolor.
			</div>
		</Loading>
	</div>
</template>

<script>
import Loading from "./components/Loading.vue";

export default {
	name: "App",
	components: {
		Loading
	},
	data() {
		return {
			isLoading: true
		};
	},
	methods: {
		handleLoading() {
			this.isLoading = !this.isLoading;
		}
	}
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");

* {
	font-family: "Roboto", sans-serif;
}

table {
	border: 1px solid #333;
	border-collapse: collapse;

	th,
	td {
		border: 1px solid #333;

		padding: 10px;
	}

	tr {
		td {
			div.loading-item {
				min-width: 100px !important;

				margin-bottom: 0;
			}
		}
	}
}

.btn {
	width: 110px;
	height: 30px;

	border: none;
	border-radius: 6px;

	background-color: tomato;

	color: #fff;

	font-weight: 500;

	margin-bottom: 20px;
}
</style>
