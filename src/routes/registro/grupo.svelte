<script lang="ts">
    let nombre_mat = ["Diseño de Software","Aseguramiento de Calidad","Sistemas Inteligentes de Negocios"];
    let nombre_maestro = ["Irma Amaya","Carlos Alemán","Lucía Beltrán"];
    let dia_1 = ["Lunes","Martes","Miércoles"];
    let dia_2 = ["Miércoles","Viernes","Jueves"];
    let horario = ["2:00 p.m.","4:00 p.m.","8:00 p.m."]

    let maxLen:number = Math.max(nombre_mat.length, nombre_maestro.length, dia_1.length, dia_2.length, horario.length);
</script>

<form class="mt-4">
    <div class="mb-3">
      <label for="exampleInputEmail1" class="form-label">Nombre de la Materia</label>
      <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Sistemas de Bases de Datos">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Nombre del maestro</label>
        <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Irma Amaya">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Día 1</label>
        <select class="form-select" aria-label="Default select example">
            <option selected>Selecciona un día</option>
            <option value="lunes">Lunes</option>
            <option value="martes">Martes</option>
            <option value="miercoles">Miércoles</option>
            <option value="jueves">Jueves</option>
            <option value="viernes">Viernes</option>
            <option value="sabado">Sábado</option>
          </select>
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Día 2</label>
        <select class="form-select" aria-label="Default select example">
            <option selected>Selecciona un día</option>
            <option value="lunes">Lunes</option>
            <option value="martes">Martes</option>
            <option value="miercoles">Miércoles</option>
            <option value="jueves">Jueves</option>
            <option value="viernes">Viernes</option>
            <option value="sabado">Sábado</option>
          </select>
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Horario</label>
        <input type="time" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Irma Amaya">
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
</form>

<div class="d-flex mt-4">
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th scope="col">Materia</th>
          <th scope="col">Maestro</th>
          <th scope="col">Día 1</th>
          <th scope="col">Día 2</th>
          <th scope="col">Horario</th>
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
          {#if Array.isArray(nombre_mat)}
            <td>{nombre_mat[0]}</td>
          {:else}
            <td>Nothing</td>
          {/if}
          {#if Array.isArray(nombre_maestro)}
            <td>{nombre_maestro[0]}</td>
          {:else}
            <td>Nothing</td>
          {/if}
          {#if Array.isArray(dia_1)}
          <td>{dia_1[0]}</td>
        {:else}
          <td>Nothing</td>
        {/if}
        {#if Array.isArray(dia_2)}
        <td>{dia_2[0]}</td>
        {:else}
            <td>Nothing</td>
        {/if}
        {#if Array.isArray(horario)}
        <td>{horario[0]}</td>
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
            {#if Array.isArray(nombre_mat) && i+1 < nombre_mat.length}
              <td>{nombre_mat[i+1]}</td>
            {:else}
              <td></td>
            {/if}
            {#if Array.isArray(nombre_maestro) && i+1 < nombre_maestro.length}
              <td>{nombre_maestro[i+1]}</td>
            {:else}
              <td></td>
            {/if}
            {#if Array.isArray(dia_1) && i+1 < dia_1.length}
            <td>{dia_1[i+1]}</td>
            {:else}
            <td></td>
            {/if}
            {#if Array.isArray(dia_2) && i+1 < dia_2.length}
            <td>{dia_2[i+1]}</td>
            {:else}
            <td></td>
            {/if}
            {#if Array.isArray(horario) && i+1 < horario.length}
            <td>{horario[i+1]}</td>
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