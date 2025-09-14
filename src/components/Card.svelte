<script>
    let {value,target,timestamp,unit,icon}= $props();
    import { Waves } from 'lucide-svelte';
</script>

<div class='card'>
<div>
	<h1 class='header'>{icon}{value}</h1>
</div>
<div>
	<h1 class='value'>{target} {unit}</h1>
</div>
<div class='divider'></div>
<p class='time'>Last updated  {timestamp}</p>
</div>
<style>
	.card{
	width:230px;
		
		border-radius:5px;
		padding:1rem;
		margin:0;
        background-color: #23272F;
	}
	.divider{
		height:1px;
		background:gray;
	}
	.header{
		margin-top:-5px;
		font-size:20px
	}
	.value{
		margin-top:-10px;
		font-size:2.5rem;
	}
	.time{
		margin-bottom:-6px;
		margin-top:1px;
		opacity:50%;
		font-size:0.7rem;
	}
</style>