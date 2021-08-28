<script>
import Darkmode from "$lib/Darkmode.svelte";
import Images from "$lib/Images.svelte";

function bye() {
	window.close();
}
</script>

<Darkmode/>

<h1>STORE</h1>
<h2>Products</h2>

<Images/>

<div on:click={bye}>Don't Click</div>

<style global>
h1 {
    text-align: center;
	width: 500px;
	margin: auto;
	font-family: 'Poppins', sans-serif;
	color: rgb(7, 7, 7);
	letter-spacing: 5px;
}
h2 {
    text-align: center;
    text-align: center;
		width: 500px;
		margin: auto;
		font-family: 'IBM Plex Sans KR', sans-serif;
		color: gray;
		letter-spacing: 5px;
}
div {
	cursor: pointer;
	background: rgb(207, 207, 218);
	width: max-content;
	padding: 5px 10px;
	margin: auto;
}
</style>