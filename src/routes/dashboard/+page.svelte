<script lang="ts">
	import { html } from "gridjs";
  import Grid from "gridjs-svelte";

  const columns = [
    "Num. Grupo",
    "Tot. Faltas",
    { 
      name: "3 Alumnos + Faltas",
      sort: {
        enabled: false
      }
    },
    { 
      name: "Sin Derecho (Examen)",
      sort: {
        enabled: false
      }
    },
    { 
      name: "Ordinario (20% Faltas)",
      sort: {
        enabled: false
      }
    },
    { 
      name: "Extraordinario (30% Faltas)",
      sort: {
        enabled: false
      }
    },
    { 
      name: "Acciones",
      formatter: (cell: string) => html(`<a href="${cell}">Ver</a> | <a href="${cell}">Editar</a>`),
      sort: {
        enabled: false
      },
      width: "10%"
    },
  ]
    
  let groupNum:number = 8;
  let totAbsences:number = 9;
  let threeStudentsMoreAbsences:string[]|null = ["Genovefa Yaakov", "Amlaíb Quirino", "Janina Aslan"];
  let noTestRight:string[]|null = ['Rusen Puck', 'Küllike Thracius', 'Jeffery Ignàtziu', 'Matic Blahoslav', 'Diana Eulalia'];
  let ordinary:string[]|null = ['Romana Borghild', 'Küllike Thracius', 'Jeffery Ignàtziu'];
  let extraordinary:string[]|null = ['Küllike Thracius'];

  const data = [
    ['1', '13', threeStudentsMoreAbsences.join(", "), noTestRight.join(", "), ordinary.join(", "), extraordinary.join(", ")]
  ]

  const pagination = {
    enabled: true,
    limit: 10,
    summary: false
  }

  const search = {
    enabled: true
  }

  const sort = true;

  let maxLen:number = Math.max(threeStudentsMoreAbsences.length, noTestRight.length, ordinary.length, extraordinary.length);
</script>

<div class="d-flex justify-content-center">
  <h1 class="fw-bold">
    Dashboard
  </h1>
</div>
<div class="d-flex">
  <Grid {columns} {data} {pagination} {search} {sort} />
</div>
