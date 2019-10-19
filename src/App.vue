<template>
	<div class="app" id="app">
		<header class="header">
			<h1>Morse</h1>
			<nav>
				<ul>
					<li><router-link to="/">Home</router-link></li>
					<li><router-link to="/about">About</router-link></li>
				</ul>
			</nav>
		</header>
		<router-view></router-view>
	</div>
</template>

<script>

export default {
	name: 'app'
};
</script>

<style lang="scss">
html {
	box-sizing: border-box;
	font-size: 16px;
	--main-dark-color: #484848;
	--main-light-color: #dedede;
	--main-acent-color: #ffdd00;
	background-color: var( --main-light-color );
}

*, *:before, *:after {
	box-sizing: inherit;
}

body, h1, h2, h3, h4, h5, h6, p, ol, ul {
	margin: 0;
	padding: 0;
	font-weight: normal;
}

ol, ul {
	list-style: none;
}

img {
	max-width: 100%;
	height: auto;
}

.app {
	font-family: Roboto, Helvetica, Arial, sans-serif;
}

.header {
	background-color: var( --main-dark-color );
	color: var( --main-light-color );
	padding: 1em;
	text-align: center;

	li {
		margin: 0 0.2em;
		display: inline;
		a {
			color: var( --main-acent-color );
		}
	}
}
</style>
