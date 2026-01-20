<?php
$conexion = new mysqli("localhost","root","","SmartCred");
if($conexion->connect_error){
    die("Error de conexión");
}

$pagina = $_POST['pagina'] ?? 'usuario';
$accion = $_POST['accion'] ?? '';
$datos = [];

/* ================== BUSCAR POR ID O NOMBRE ================== */
if($accion == "buscar" && !empty($_POST['id'])){
    $valor = $conexion->real_escape_string($_POST['id']);
    
    if($pagina == "usuario"){
        $sql = "SELECT * FROM Usuario 
                WHERE id_usuario='$valor' 
                OR nombre LIKE '%$valor%' 
                OR apellidos LIKE '%$valor%'
                OR no_control='$valor'";
    } elseif($pagina == "libro"){
        $sql = "SELECT * FROM Libro 
                WHERE id_libro='$valor' 
                OR titulo LIKE '%$valor%'";
    } else {
        $tabla = ucfirst($pagina);
        $campo = "id_$pagina";
        $sql = "SELECT * FROM $tabla WHERE $campo='$valor'";
    }

    $resultado = $conexion->query($sql);
    if($resultado && $resultado->num_rows > 0){
        $datos = $resultado->fetch_assoc();
    }
}

/* ================== USUARIO ================== */
if($pagina=="usuario" && $accion && $accion!="buscar"){
    if($accion=="alta"){
        $conexion->query("INSERT INTO Usuario 
        (nombre,apellidos,no_control,edad,correo,foto)
        VALUES(
            '".$_POST['nombre']."',
            '".$_POST['apellidos']."',
            '".$_POST['control']."',
            ".$_POST['edad'].",
            '".$_POST['correo']."',
            '".$_POST['control'].".png'
        )");
    }
    if($accion=="modificar"){
        $conexion->query("UPDATE Usuario SET
            nombre='".$_POST['nombre']."',
            apellidos='".$_POST['apellidos']."',
            no_control='".$_POST['control']."',
            edad=".$_POST['edad'].",
            correo='".$_POST['correo']."',
            foto='".$_POST['control'].".png'
            WHERE id_usuario=".$_POST['id']);
    }
    if($accion=="eliminar"){
        $conexion->query("DELETE FROM Usuario WHERE id_usuario=".$_POST['id']);
    }
}

/* ================== AUTOR ================== */
if($pagina=="autor" && $accion && $accion!="buscar"){
    if($accion=="alta"){
        $conexion->query("INSERT INTO Autor VALUES(
            NULL,
            '".$_POST['nombre']."',
            '".$_POST['nacionalidad']."'
        )");
    }
    if($accion=="modificar"){
        $conexion->query("UPDATE Autor SET
            nombre='".$_POST['nombre']."',
            nacionalidad='".$_POST['nacionalidad']."'
            WHERE id_autor=".$_POST['id']);
    }
    if($accion=="eliminar"){
        $conexion->query("DELETE FROM Autor WHERE id_autor=".$_POST['id']);
    }
}

/* ================== LIBRO ================== */
if($pagina=="libro" && $accion && $accion!="buscar"){
    if($accion=="alta"){
        $conexion->query("INSERT INTO Libro
        (titulo,editorial,anio,imagen)
        VALUES(
            '".$_POST['titulo']."',
            '".$_POST['editorial']."',
            ".$_POST['anio'].",
            '".$_POST['id'].".png'
        )");
    }
    if($accion=="modificar"){
        $conexion->query("UPDATE Libro SET
            titulo='".$_POST['titulo']."',
            editorial='".$_POST['editorial']."',
            anio=".$_POST['anio'].",
            imagen='".$_POST['id'].".png'
            WHERE id_libro=".$_POST['id']);
    }
    if($accion=="eliminar"){
        $conexion->query("DELETE FROM Libro WHERE id_libro=".$_POST['id']);
    }
}

/* ================== EJEMPLAR ================== */
if($pagina=="ejemplar" && $accion && $accion!="buscar"){
    if($accion=="alta"){
        $conexion->query("INSERT INTO Ejemplar VALUES(
            NULL,
            '".$_POST['lugar']."'
        )");
    }
    if($accion=="modificar"){
        $conexion->query("UPDATE Ejemplar SET
            lugar='".$_POST['lugar']."'
            WHERE id_ejemplar=".$_POST['id']);
    }
    if($accion=="eliminar"){
        $conexion->query("DELETE FROM Ejemplar WHERE id_ejemplar=".$_POST['id']);
    }
}

/* ================== PRESTAMO ================== */
if($pagina=="prestamo" && $accion && $accion!="buscar"){
    if($accion=="alta"){
        $conexion->query("INSERT INTO Prestamo VALUES(
            NULL,
            '".$_POST['fecha_prestamo']."',
            '".$_POST['fecha_limite']."',
            '".$_POST['usuario']."',
            '".$_POST['libro']."',
            '".$_POST['estado']."'
        )");
    }
    if($accion=="modificar"){
        $conexion->query("UPDATE Prestamo SET
            fecha_prestamo='".$_POST['fecha_prestamo']."',
            fecha_limite='".$_POST['fecha_limite']."',
            nombre_usuario='".$_POST['usuario']."',
            titulo_libro='".$_POST['libro']."',
            estado='".$_POST['estado']."'
            WHERE id_prestamo=".$_POST['id']);
    }
    if($accion=="eliminar"){
        $conexion->query("DELETE FROM Prestamo WHERE id_prestamo=".$_POST['id']);
    }
}
?>
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Sistema Bibliotecario CECyTEM</title>

<style>
body{
    font-family:'Segoe UI',Arial,sans-serif;
    background:linear-gradient(135deg,#0f3d2e,#1b5e20);
    min-height:100vh;
    margin:0;
}
.header{
    background:white;
    border-bottom:5px solid #1b5e20;
    padding:15px;
    text-align:center;
}
.box{
    width:520px;
    margin:30px auto;
    background:white;
    padding:30px;
    border-radius:20px;
    box-shadow:0 15px 35px rgba(0,0,0,.4);
    border-top:8px solid #1b5e20;
}
h2{ text-align:center;color:#1b5e20;}
input{width:100%;padding:12px;margin:6px 0;border-radius:8px;border:1px solid #ccc;}
button{width:100%;padding:12px;margin:6px 0;border:none;border-radius:10px;font-weight:bold;cursor:pointer;}
button[value="alta"]{background:#1b5e20;color:white;}
button[value="modificar"]{background:#2e7d32;color:white;}
button[value="eliminar"]{background:black;color:white;}
.buscar{background:#4caf50;color:white;}
.nav{display:flex;justify-content:space-between;margin-top:15px;}
.nav button{width:48%;background:white;color:#1b5e20;border:2px solid #1b5e20;}
.nav button:hover{background:#1b5e20;color:white;}
img{display:block;margin:10px auto;border-radius:10px;}
</style>
</head>

<body>

<div class="header">
<h1>📚 SISTEMA BIBLIOTECARIO CECyTEM</h1>
<p>Control de Usuarios, Autores, Libros, Ejemplares y Préstamos</p>
</div>

<div class="box">
<form method="post">
<input type="hidden" name="pagina" value="<?= $pagina ?>">

<?php if($pagina=="usuario"){ ?>
<h2>👤 USUARIO</h2>
<input name="id" placeholder="ID, No. Control o Nombre">
<input name="nombre" placeholder="Nombre" value="<?= $datos['nombre'] ?? '' ?>">
<input name="apellidos" placeholder="Apellidos" value="<?= $datos['apellidos'] ?? '' ?>">
<input name="control" placeholder="No. Control" value="<?= $datos['no_control'] ?? '' ?>">
<input name="edad" placeholder="Edad" value="<?= $datos['edad'] ?? '' ?>">
<input name="correo" placeholder="Correo" value="<?= $datos['correo'] ?? '' ?>">

<?php 
$fotoUsuario = $datos['foto'] ?? 'default.jpg';
?>
<img src="imagenes/usuarios/<?= $fotoUsuario ?>" width="150">

<?php } elseif($pagina=="autor"){ ?>
<h2>✍️ AUTOR</h2>
<input name="id" placeholder="ID">
<input name="nombre" placeholder="Nombre" value="<?= $datos['nombre'] ?? '' ?>">
<input name="nacionalidad" placeholder="Nacionalidad" value="<?= $datos['nacionalidad'] ?? '' ?>">

<?php } elseif($pagina=="libro"){ ?>
<h2>📘 LIBRO</h2>
<input name="id" placeholder="ID o Título">
<input name="titulo" placeholder="Título" value="<?= $datos['titulo'] ?? '' ?>">
<input name="editorial" placeholder="Autor / Editorial" value="<?= $datos['editorial'] ?? '' ?>">
<input name="anio" placeholder="Año" value="<?= $datos['anio'] ?? '' ?>">

<?php 
$fotoLibro = $datos['imagen'] ?? 'default.png';
?>
<img src="imagenes/libros/<?= $fotoLibro ?>" width="120">

<?php } elseif($pagina=="ejemplar"){ ?>
<h2>📦 EJEMPLAR</h2>
<input name="id" placeholder="ID">
<input name="lugar" placeholder="Lugar" value="<?= $datos['lugar'] ?? '' ?>">

<?php } elseif($pagina=="prestamo"){ ?>
<h2>📅 PRÉSTAMO</h2>
<input name="id" placeholder="ID">
<input type="date" name="fecha_prestamo" value="<?= $datos['fecha_prestamo'] ?? '' ?>">
<input type="date" name="fecha_limite" value="<?= $datos['fecha_limite'] ?? '' ?>">
<input name="usuario" placeholder="Usuario" value="<?= $datos['nombre_usuario'] ?? '' ?>">
<input name="libro" placeholder="Libro" value="<?= $datos['titulo_libro'] ?? '' ?>">
<input name="estado" placeholder="Estado" value="<?= $datos['estado'] ?? '' ?>">
<?php } ?>

<button name="accion" value="alta">ALTA</button>
<button name="accion" value="modificar">MODIFICAR</button>
<button name="accion" value="eliminar">ELIMINAR</button>
<button name="accion" value="buscar" class="buscar">🔍 BUSCAR</button>
</form>

<form method="post" class="nav">
<?php if($pagina!="usuario"){ ?>
<button name="pagina" value="<?= $pagina=="autor"?"usuario": ($pagina=="libro"?"autor": ($pagina=="ejemplar"?"libro":"ejemplar")) ?>">⬅️ ANTERIOR</button>
<?php } ?>

<?php if($pagina!="prestamo"){ ?>
<button name="pagina" value="<?= $pagina=="usuario"?"autor": ($pagina=="autor"?"libro": ($pagina=="libro"?"ejemplar":"prestamo")) ?>">SIGUIENTE ➡️</button>
<?php } ?>
</form>
</div>

</body>
</html>
