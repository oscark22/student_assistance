<script lang="ts">
    let alum_nombre = ["Ramiro","Andrés","Carlos"];
    let alum_ap = ["Núñez","De Anda","Sandez"];
    let alum_am = ["Sánchez","Rivera",""];
    let alum_matricula = ["e01267","e02736","e012863"];
    let grupos = ["100","101","102"]

    let maxLen:number = Math.max(alum_nombre.length, alum_ap.length, alum_am.length, alum_matricula.length, grupos.length);
</script>

<form class="mt-4">
    <div class="mb-3">
      <label for="exampleInputEmail1" class="form-label">Nombre del Alumno</label>
      <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Ramiro">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Apellido paterno del Alumno</label>
        <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Núñez">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Apellido materno del Alumno</label>
        <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Sánchez">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Grupo</label>
        <select class="form-select" aria-label="Default select example">
            <option selected>Selecciona un grupo</option>
            <option value="100">100</option>
            <option value="101">101</option>
            <option value="102">102</option>
            <option value="103">103</option>
            <option value="104">104</option>
            <option value="105">105</option>
          </select>
    </div>
    <div class="mb-3">
      <label for="exampleInputPassword1" class="form-label">Matrícula</label>
      <input type="text" class="form-control" id="exampleInputPassword1" placeholder="e012667">
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
</form>

<div class="d-flex mt-4">
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido Paterno</th>
          <th scope="col">Apellido Materno</th>
          <th scope="col">Matrícula</th>
          <th scope="col">Grupo</th>
          <th scope="col" class="text-center">
          </th>
          <th scope="col" class="text-center">
          </th>
          <th scope="col" class="text-center">
          </th>
        </tr>
      </thead>
      <tbody>
        <!-- TODO each per group -->
        <tr>
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
        {#if Array.isArray(alum_matricula)}
        <td>{alum_matricula[0]}</td>
        {:else}
            <td>Nothing</td>
        {/if}
        {#if Array.isArray(grupos)}
        <td>{grupos[0]}</td>
        {:else}
        <td>Nothing</td>
        {/if}
          <td class="text-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-eye" viewBox="0 0 16 16">
              <path d="M16 8s-3-5.5-8-5.5S0 8 0 8s3 5.5 8 5.5S16 8 16 8zM1.173 8a13.133 13.133 0 0 1 1.66-2.043C4.12 4.668 5.88 3.5 8 3.5c2.12 0 3.879 1.168 5.168 2.457A13.133 13.133 0 0 1 14.828 8c-.058.087-.122.183-.195.288-.335.48-.83 1.12-1.465 1.755C11.879 11.332 10.119 12.5 8 12.5c-2.12 0-3.879-1.168-5.168-2.457A13.134 13.134 0 0 1 1.172 8z"/>
              <path d="M8 5.5a2.5 2.5 0 1 0 0 5 2.5 2.5 0 0 0 0-5zM4.5 8a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0z"/>
            </svg>
          </td>
          <td class="text-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pen" viewBox="0 0 16 16">
              <path d="m13.498.795.149-.149a1.207 1.207 0 1 1 1.707 1.708l-.149.148a1.5 1.5 0 0 1-.059 2.059L4.854 14.854a.5.5 0 0 1-.233.131l-4 1a.5.5 0 0 1-.606-.606l1-4a.5.5 0 0 1 .131-.232l9.642-9.642a.5.5 0 0 0-.642.056L6.854 4.854a.5.5 0 1 1-.708-.708L9.44.854A1.5 1.5 0 0 1 11.5.796a1.5 1.5 0 0 1 1.998-.001zm-.644.766a.5.5 0 0 0-.707 0L1.95 11.756l-.764 3.057 3.057-.764L14.44 3.854a.5.5 0 0 0 0-.708l-1.585-1.585z"/>
            </svg>
          </td>
          <td class="text-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-trash" viewBox="0 0 16 16">
              <path d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0V6z"/>
              <path fill-rule="evenodd" d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1v1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4H4.118zM2.5 3V2h11v1h-11z"/>
            </svg>
          </td>
        </tr>
        {#each Array(maxLen-1) as _, i (i)}
          <tr>
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
            {#if Array.isArray(alum_matricula) && i+1 < alum_matricula.length}
            <td>{alum_matricula[i+1]}</td>
            {:else}
            <td></td>
            {/if}
            {#if Array.isArray(grupos) && i+1 < grupos.length}
            <td>{grupos[i+1]}</td>
            {:else}
            <td></td>
            {/if}
            <td class="text-center">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-eye" viewBox="0 0 16 16">
                  <path d="M16 8s-3-5.5-8-5.5S0 8 0 8s3 5.5 8 5.5S16 8 16 8zM1.173 8a13.133 13.133 0 0 1 1.66-2.043C4.12 4.668 5.88 3.5 8 3.5c2.12 0 3.879 1.168 5.168 2.457A13.133 13.133 0 0 1 14.828 8c-.058.087-.122.183-.195.288-.335.48-.83 1.12-1.465 1.755C11.879 11.332 10.119 12.5 8 12.5c-2.12 0-3.879-1.168-5.168-2.457A13.134 13.134 0 0 1 1.172 8z"/>
                  <path d="M8 5.5a2.5 2.5 0 1 0 0 5 2.5 2.5 0 0 0 0-5zM4.5 8a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0z"/>
                </svg>
            </td>
            <td class="text-center">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pen" viewBox="0 0 16 16">
                  <path d="m13.498.795.149-.149a1.207 1.207 0 1 1 1.707 1.708l-.149.148a1.5 1.5 0 0 1-.059 2.059L4.854 14.854a.5.5 0 0 1-.233.131l-4 1a.5.5 0 0 1-.606-.606l1-4a.5.5 0 0 1 .131-.232l9.642-9.642a.5.5 0 0 0-.642.056L6.854 4.854a.5.5 0 1 1-.708-.708L9.44.854A1.5 1.5 0 0 1 11.5.796a1.5 1.5 0 0 1 1.998-.001zm-.644.766a.5.5 0 0 0-.707 0L1.95 11.756l-.764 3.057 3.057-.764L14.44 3.854a.5.5 0 0 0 0-.708l-1.585-1.585z"/>
                </svg>
            </td>
            <td class="text-center">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-trash" viewBox="0 0 16 16">
                    <path d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0V6z"/>
                    <path fill-rule="evenodd" d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1v1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4H4.118zM2.5 3V2h11v1h-11z"/>
                </svg>
            </td>
          </tr>
        {/each}
        <!-- END  -->
      </tbody>
    </table>
  </div>