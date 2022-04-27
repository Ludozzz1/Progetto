<script>
	import Geoidi from './Geoidi.svelte'
	import NavBar from './NavBar.svelte'
	import Introduction from './Introduction.svelte'
	import GlobalGeoids from './GlobalGeoids.svelte'
	import Submit from './Submit.svelte'
	import World from './World.svelte'
	let array = ['Italia 1','Italia 37','Lombardia', 'Champagne', 'Francia','Svizzera Ovest']
</script>

<main>	
	<NavBar></NavBar>
	<Introduction></Introduction>
	<GlobalGeoids></GlobalGeoids>
	<nav class="level">
		<div class="level-left">
			<div class="level-item">
				<div class='columns section'>
					<Geoidi list={array}></Geoidi>
				</div>
			</div>
		</div>
		<World></World>
	</nav>
	<Submit></Submit>
</main>