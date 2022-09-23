<script>
	import Alumno from './alumno.svelte';
	import Materia from './materia.svelte';
	import Grupo from './grupo.svelte';

	let alum = false;
	let group = false;
	let mat = false;


	function change_alum(){
		alum = true;
		group = false;
		mat = false;
	}
	function change_mat(){
		alum = false;
		group = false;
		mat = true;
	}
	function change_group(){
		alum = false;
		group = true;
		mat = false;
	}
</script>

<button type="button" class="btn btn-outline-primary col-3 mx-5" on:click={() => change_mat()}>Registrar Materia</button>

<button type="button" class="btn btn-outline-primary col-3 mx-5" on:click={() => change_group()}>Registrar Grupo</button>

<button type="button" class="btn btn-outline-primary col-3 mx-5" on:click={() => change_alum()}>Registrar Alumno</button>

{#if alum}
	<Alumno />
{/if}
{#if mat}
	<Materia />
{/if}
{#if group}
	<Grupo />
{/if}