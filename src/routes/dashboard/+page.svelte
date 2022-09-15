<script lang="ts">
  let groupNum:number = 8;
  let totAbsences:number = 9;
  let threeStudentsMoreAbsences:string[] = ["Genovefa Yaakov", "Amlaíb Quirino", "Janina Aslan"];
  let noTestRight:string[] = ['Rusen Puck', 'Küllike Thracius', 'Jeffery Ignàtziu', 'Matic Blahoslav', 'Diana Eulalia'];
  let ordinary:string[] = ['Romana Borghild', 'Küllike Thracius', 'Jeffery Ignàtziu'];
  let extraordinary:string[] = ['Küllike Thracius'];
</script>

<div class="d-flex justify-content-center">
  <h1 class="fw-bold">
    Dashboard
  </h1>
</div>
<div class="mt-4">
  <table class="table">
    <thead>
      <tr>
        <th scope="col">Num. Grupo</th>
        <th scope="col">Tot. Faltas</th>
        <th scope="col">3 Alumnos + Faltas</th>
        <th scope="col">Sin Derecho (Examen)</th>
        <th scope="col">Ordinario (20% Faltas)</th>
        <th scope="col">Extraordinario (30% Faltas)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row" rowspan="5">1</th>
        <td rowspan="5">1</td>
        <td rowspan="1">1</td>
        <td rowspan="1">1</td>
        <td rowspan="1">1</td>
        <td rowspan="1">1</td>
      </tr>
      <tr>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
      </tr>
    </tbody>
  </table>
</div>