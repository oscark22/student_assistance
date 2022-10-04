<script lang="ts">
    let alum_nombre = ["Ramiro","Andrés","Carlos"];
    let alum_ap = ["Núñez","De Anda","Sandez"];
    let alum_am = ["Sánchez","Rivera",""];
    let alum_matricula = ["e01267","e02736","e012863"];
	let asistencias = ["9","8","9"];
	let inasistencias = ["0","1","0"]

    let maxLen:number = Math.max(alum_nombre.length, alum_ap.length, alum_am.length, alum_matricula.length);
</script>

<h1>Exportar archivo</h1>

<form class="mt-10">
	<div class="mt-6 container">
		<div class="mt-6 row">
			<div class="mb-3 col">
				<label for="materia1" class="form-label">Seleccione una materia: </label>
				<select class="form-select" aria-label="Default select example" id="materia1">
					<option selected hidden>Materia</option>
					<option value="ICC102">Sistemas Operativos</option>
					<option value="ISW100">Diseño de Software</option>
					<option value="ICC101">Sistemas de Bases de Datos</option>
				</select>
			</div>
			<div class="mb-3 col">
				<label for="periodo1" class="form-label">Seleccione un periodo: </label>
				<select class="form-select" aria-label="Default select example" id="periodo1">
					<option selected hidden>Periodo</option>
					<option value="EneroJunio2022">Enero-Junio(2022)</option>
					<option value="AgostoDiciembre2022">Agosto-Diciembre(2022)</option>
				</select>
			</div>
		</div>
	</div>
</form>
<div class="d-flex mt-4">
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th scope="col">Matrícula</th>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido Paterno</th>
          <th scope="col">Apellido Materno</th>
		      <th scope="col">Asistencias</th>
          <th scope="col">Inasistencias</th>
        </tr>
      </thead>
      <tbody>
        <!-- TODO each per group -->
        <tr>
          {#if Array.isArray(alum_matricula)}
          <td>{alum_matricula[0]}</td>
          {:else}
    	    <td>Nothing</td>
          {/if}
          {#if Array.isArray(alum_nombre)}
            <td>{alum_nombre[0]}</td>
          {:else}
            <td>Nothing</td>
          {/if}
          {#if Array.isArray(alum_ap)}
            <td>{alum_ap[0]}</td>
          {:else}
            <td>Nothing</td>
          {/if}
          {#if Array.isArray(alum_am)}
          <td>{alum_am[0]}</td>
        {:else}
          <td>Nothing</td>
        {/if}
        
		{#if Array.isArray(asistencias)}
            <td>{asistencias[0]}</td>
          {:else}
            <td>Nothing</td>
          {/if}
		  {#if Array.isArray(inasistencias)}
		  <td>{inasistencias[0]}</td>
		{:else}
		  <td>Nothing</td>
		{/if}
        </tr>
        {#each Array(maxLen-1) as _, i (i)}
          <tr>
            {#if Array.isArray(alum_matricula) && i+1 < alum_matricula.length}
            <td>{alum_matricula[i+1]}</td>
            {:else}
            <td></td>
            {/if}
            {#if Array.isArray(alum_nombre) && i+1 < alum_nombre.length}
              <td>{alum_nombre[i+1]}</td>
            {:else}
              <td></td>
            {/if}
            {#if Array.isArray(alum_ap) && i+1 < alum_ap.length}
              <td>{alum_ap[i+1]}</td>
            {:else}
              <td></td>
            {/if}
            {#if Array.isArray(alum_am) && i+1 < alum_am.length}
            <td>{alum_am[i+1]}</td>
            {:else}
            <td></td>
            {/if}

			{#if Array.isArray(asistencias) && i+1 < asistencias.length}
            <td>{asistencias[i+1]}</td>
            {:else}
            <td></td>
            {/if}
			{#if Array.isArray(inasistencias) && i+1 < inasistencias.length}
            <td>{inasistencias[i+1]}</td>
            {:else}
            <td></td>
            {/if}
          </tr>
        {/each}
        <!-- END  -->
      </tbody>
    </table>
  </div>
<div>
	<button type="button" class="btn btn-outline-primary mx-5">
		Exportar
	</button>
</div>