 <title> APLICACION PRUEBA</title> 
<!DOCTYPE html>
<html lang="me">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>APLICACION PRUEBA </title>

    <!-- Bootstrap -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
</head>
</body>
<div class="appPRUEBA" id="appPRUEBA">
    <div class="container-fluid">
        <div class="card text-white" id="carNombre">
            <div class="card-header bg-primary">
                Registro de Nombres
  <button type="button" class="btn-close text-end" data-bs-dismiss="alert" data-bs-target="#carNombre" aria-label="Close"></button>
  </div>
  <div class="card-body text-dark"> 
  <form method="post" @submit.prevent="GuardarPersona" @reset="PersonaNueva"></form>      
  <div class="row p-1">
  <div class="col col-md-2">Codigo:</div>         
  <div class="col col-md-2">
  <input title="Ingrese el codigo" v-model="Persona.Codigo" pattern="[0-9]{3,10}" required type="text" class="form-control">  
  </div>
  <div class="row p-1">
<div class="col col-md-2">Nombre:</div>
<div class="col col-md-3">
<input title="Ingrese Nombre de alumno" v-model="Persona.Nombre" pattern="[A-Za-zñÑáéíóúü ]{3,75}" required type="text" class="form-control">
</div>
</div>  
 <div class="row p-1">
<div class="col col-md-2">Direccion:</div>
<div class="col col-md-3">
<input title="Ingrese la direccion" v-model="Perona.direccion" pattern="[A-Za-zñÑáéíóúü ]{3,100}" required type="text" class="form-control">
</div>
</div>
lass="row p-1">
    <div class="col col-md-5 text-center">
        <div v-if="Persona.mostrar_msg" class="alert alert-primary alert-dismissible fade show" role="alert">
            {{ Persona.msg }}
            <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
        </div>
    </div>
</div>
<div class="row m-2">
    <div class="col col-md-5 text-center">
        <input class="btn btn-success" type="submit" value="Guardar Persona">
        <input class="btn btn-warning" type="reset" value="Persona Nueva">
    </div>
</div>
</form>
</div>
</div>
<div class="card text-white" id="carBuscarpersona">
<div class="card-header bg-primary">
    Busqueda De las Personas

<button type="button" class="btn-close" data-bs-dismiss="alert" data-bs-target="#carBuscarNombre" aria-label="Close"></button>
</div>
<div class="card-body">
    <table class="table table-dark table-hover">
        <thead>
            <tr>
                <th colspan="6">

 Buscar: <input @keyup="Buscando Persona" v-model="Buscar" placeholder="Busqueda de Persona " class="form-control" type="text" >
    </th>
</tr>
</tr>

<th>CODIGO</th>
<th>NOMBRE</th>
<th>DIRECCION</th>
<th></th>
 </tr>
</thead>
</tbody>
<tr v-for="item in persona" @click='Modificarpersona( item )' :key="item.idpersona">
        <td>{{item.Codigo}}</td>
        <td>{{item.Nombre}}</td>
        <td>{{item.Direccion}}</td>
        <td>
<button class="btn btn-danger" @click="EliminarAlumno(item)">Eliminar</button>
 </td>
</tr>
 </tbody>
</table>
 </div>
</div>
</div>
 </div>
 <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" 
        integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <script>
