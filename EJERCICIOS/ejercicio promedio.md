# EJERCICIO

## VERSION 1 

calcular el promeddio de un estudiante de PILARES

primer periodo

taller:6.7

computo; 8.0
    
segundo periodo

taller:5.7

computo; 9
    
tercer periodo

taller:9.92

computo; 6.8
    
calcular y mostrar por consola promedio por periodo y promedio general, ademas del status APROBADO o REPROBADO.

        var taller= parseInt(prompt("Ingresa la calificacion de taller"));
        var computo = parseInt(prompt("Ingresa la calificacion de computo"));;
        var periodo1 = (taller + computo)/2;
        console.log("Periodo 1: "  + periodo1);
        taller= parseInt(prompt("Ingresa la calificacion de taller"));
        computo = parseInt(prompt("Ingresa la calificacion de computo"));
        var periodo2 = (taller + computo)/2;
        console.log("Periodo 2: "  + periodo2);
        taller= parseInt(prompt("Ingresa la calificacion de taller"));
        computo = parseInt(prompt("Ingresa la calificacion de computo"));
        var periodo3 = (taller + computo)/2;
        console.log("Periodo 3: "  + periodo3);
        var promedio = (periodo1 + periodo2 + periodo3) / 3;
        
        console.log("Promedio: "  + promedio);
        
        if(promedio > 6){
            console.log("APROBADO");
        }else{
            console.log("REPROBADO");
        }

## VERSION 2
Se deben solicitar por prompt las calificaciones y además agregar el nombre del estudiante, también su estatus de acuerdo al promedio general, menor de 6 es REPROBADO, de 6.1 a 8 es BIEN, de 8.1 a 9 es MUY BIEN y de 9.1 a 10 es EXCELENTE.

        var captura = confirm("Deseas capturar un alumno ");
        if(captura == true){
            var calificacion = parseFloat(prompt("ingresa la calificación"));
            var suma = 0;
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            var periodo1 = suma / 3;
            suma = 0;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            var periodo2 = suma/3;
            suma = 0;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            calificacion = parseFloat(prompt("ingresa la calificación"));
            suma = suma + calificacion;
            var periodo3 = suma/3;
            var promedio = (periodo1  + periodo2 + periodo3)/3;
            // alert("periodo 1: "  + periodo1 + "\nperiodo2: " + periodo2);
            alert(`periodo 1: ${periodo1} \nperiodo2: ${periodo2} \nperiodo3: ${periodo3} \npromedio: ${promedio} `);
        
            switch(true){
                case promedio < 6:
                    alert("REPROBADO");
                    break;
                case promedio < 8:
                    alert("BIEN");
                    break;
                case promedio < 10:
                    alert("MUY BIEN");
                    break;
                case promedio == 10:
                    alert("EXCELENTE");
                    break;
            }
        
        }else{
            alert("Adios ");
        }


## VERSION 3
Se deben pedir datos de N número de alumnos y los periodos deben estar en ciclo

    var captura = confirm("Deseas capturar un alumno ");
    
    while(captura == true){
        var sumaPeriodo = 0;
        for(var j = 0;j < 3;j++){
            var suma = 0;
            var promedioPeriodo=0;
            for(var i = 0;i < 3; i++){
                var calificacion = parseFloat(prompt(`ingresa la calificación ${i +1} del periodo ${j+1}`));
                var suma = suma + calificacion;
            }
            promedioPeriodo = suma/3;
            alert(`promedio del periodo  ${j + 1} = ${promedioPeriodo}`);
            sumaPeriodo = sumaPeriodo + promedioPeriodo;
        }
        var promedio = sumaPeriodo/3;
    
        switch(true){
            case promedio < 6:
                alert(`REPROBADO, PROMEDIO: ${promedio}`);
                break;
            case promedio < 8:
                alert(`BIEN, PROMEDIO: ${promedio}`);
                break;
            case promedio < 10:
                alert(`MUY BIEN, PROMEDIO: ${promedio}`);
                break;
            case promedio == 10:
                alert(`EXCELENTE, PROMEDIO: ${promedio}`);
                break;
        }
    
        captura = confirm("Deseas capturar un alumno ");
    }
    alert("Adios ");



## VERSION 4
Se debe agregar la fecha de las calificaciones y poder visualizalas

![image](https://github.com/user-attachments/assets/ef1eb5f4-f3c6-4295-9142-850ec73c6add)

![image](https://github.com/user-attachments/assets/55b015e7-38a9-4818-a56d-baf3fdb26daa)



## VERSION 5
Utilizar arreglos para almacenar los nombres de los alumnos.

    var captura = confirm("Deseas capturar un alumno ");
    var nombres = new Array();
     while(captura == true){
        
        var nombre = prompt("Ingresa el nombre del alumno");
        nombres.push(nombre); 
        
        captura = confirm("Deseas capturar un alumno ");
     }
     alert("Adios ");
    
    //  //impresión de todo el arreglo
    //  console.log(nombres);
    //  nombres.pop();
    //  console.log(nombres);
    //  nombres.unshift("Pedro");
    //  nombres.shift();
    
    //  nombres1 = ["Andrea","Araceli","María","Angela"];
    
    //  var nombresUnidos=nombres.concat(nombres1);
    //  nombresUnidos.sort();
    //  console.log(nombresUnidos);
    //  nombresUnidos.reverse();
    //  console.log(nombresUnidos);
    
    // s
    
    //  //Recorrido del arreglo
    //  for(var i = 0;i < nombres.length;i++){
    //     console.log(nombres[i]);
    //     if(nombres[i] == "Juan"){
    //         break;
    //     }
    //  }

Almacenar las calificaciones, los promedios de periodo de cada alumno

        var captura = confirm("¿Deseas capturar un alumno?");
        var nombres = [];
        var calificaciones = []; //matriz de matrices que almacena todas las calificaciones por alumno
        
        while (captura) {
            var nombre = prompt("Ingresa el nombre del alumno");
            nombres.push(nombre);
        
            var calPeriodo = []; //almacenara las calificaciones en una matriz por alumno
            for (var j = 0; j < 3; j++) {
                var calificacionesAlumno = []; //arreglo de una linea
                var sumaCalificaciones = 0;
                for (var i = 0; i < 3; i++) {
                    var calificacion = parseFloat(prompt("Ingresa la calificación " + (i + 1) + " del periodo " + (j + 1)));
                    calificacionesAlumno.push(calificacion);
                    sumaCalificaciones += calificacion;
                    console.log("calificacionesAlumno: "  + calificacionesAlumno);
                }
                calPeriodo.push(calificacionesAlumno);
                var promedioPeriodo = sumaCalificaciones / 3;
                console.log("Promedio del periodo " + (j + 1) + " para " + nombre + ": " + promedioPeriodo);
                console.log("calPeriodo " + calPeriodo);
            }
            calificaciones.push(calPeriodo);
        
            captura = confirm("¿Deseas capturar otro alumno?");
        }
        
        alert("Adiós");
        console.log(calificaciones);



mostrarlos con los nombres correspondietes.

    var captura = confirm("¿Deseas capturar un alumno?");
    var nombres = [];
    var calificaciones = []; //matriz de matrices que almacena todas las calificaciones por alumno
    var promedioAlumnno = [];
    while (captura) {
        var nombre = prompt("Ingresa el nombre del alumno");
        nombres.push(nombre);
    
        var calPeriodo = []; //almacenara las calificaciones en una matriz por alumno
        for (var j = 0; j < 3; j++) {
            var calificacionesAlumno = []; //arreglo de una linea
            var sumaCalificaciones = 0;
            for (var i = 0; i < 3; i++) {
                var calificacion = parseFloat(prompt("Ingresa la calificación " + (i + 1) + " del periodo " + (j + 1)));
                calificacionesAlumno.push(calificacion);
                sumaCalificaciones += calificacion;
            }
            calPeriodo.push(calificacionesAlumno);
            var promedioPeriodo = sumaCalificaciones / 3;
            console.log("Promedio del periodo " + (j + 1) + " para " + nombre + ": " + promedioPeriodo);
            
    
        }
        promedioAlumnno.push(promedioPeriodo);
        calificaciones.push(calPeriodo);
        captura = confirm("¿Deseas capturar otro alumno?");
    }
    
    alert("Adiós");
    for(var i = 0;i < 3;i++ ){
        console.log("nombre: " + nombres[i] + " Promedio: " + promedioAlumnno[i]);
    }

## VERSION 6
Utilizar funciones para optimizar el programa

![image](https://github.com/user-attachments/assets/30a4afbc-cf4e-4d6f-94c0-426869ad1ca4)

        // Función para pedir el nombre del alumno
        function pedirNombre() {
            var nombre = prompt("Ingresa el nombre del alumno");
            return nombre;
        }
        
        // Función para pedir las calificaciones de un alumno
        function pedirCalificaciones() {
            var calificaciones = [];
            for (var i = 0; i < 3; i++) {
                var calificacion = parseFloat(prompt("Ingresa la calificación " + (i + 1)));
                calificaciones.push(calificacion);
            }
            return calificaciones;
        }
        
        // Función para calcular el promedio de las calificaciones
        function calcularPromedio(calificaciones) {
            var suma = 0;
            for (var i = 0; i < calificaciones.length; i++) {
                suma += calificaciones[i];
            }
            var promedio = suma / calificaciones.length;
            return promedio;
        }
        
        // Función principal para capturar datos y mostrar resultados
        function capturarDatos() {
            var nombres = [];
            var promedios = [];
            var captura = confirm("¿Deseas capturar un alumno?");
        
            while (captura) {
                var nombre = pedirNombre();
                var calificaciones = pedirCalificaciones();
                var promedio = calcularPromedio(calificaciones);
        
                nombres.push(nombre);
                promedios.push(promedio);
        
                captura = confirm("¿Deseas capturar otro alumno?");
            }
        
            alert("Adiós");
        
            // Mostrar nombres y promedios
            for (var i = 0; i < nombres.length; i++) {
                console.log("Nombre: " + nombres[i] + ", Promedio: " + promedios[i]);
            }
        }
        
        // Llamar a la función principal para iniciar el proceso
        capturarDatos();

## VERSION 7
Metodos de texto

        // Función para pedir el nombre del alumno con validación usando length y toUpperCase
        function pedirNombre() {
            var nombre = "";
            while (!nombre || nombre.length < 3) {  // Validamos que el nombre tenga al menos 3 caracteres
                nombre = prompt("Ingresa el nombre del alumno (mínimo 3 caracteres)");
                if (!nombre || nombre.length < 3) {
                    alert("El nombre debe tener al menos 3 caracteres. Inténtalo de nuevo.");
                }
            }
            nombre = nombre.toUpperCase();  // Convertir el nombre a mayúsculas
            return nombre;
        }
        
        // Función para pedir las calificaciones de un alumno
        function pedirCalificaciones() {
            var calificaciones = [];
            for (var i = 0; i < 3; i++) {
                var calificacion = parseFloat(prompt("Ingresa la calificación " + (i + 1)));
                calificaciones.push(calificacion);
            }
            return calificaciones;
        }
        
        // Función para calcular el promedio de las calificaciones
        function calcularPromedio(calificaciones) {
            var suma = 0;
            for (var i = 0; i < calificaciones.length; i++) {
                suma += calificaciones[i];
            }
            var promedio = suma / calificaciones.length;
            return promedio;
        }
        
        // Función principal para capturar datos y mostrar resultados
        function capturarDatos() {
            var nombres = [];
            var promedios = [];
            var captura = confirm("¿Deseas capturar un alumno?");
        
            while (captura) {
                var nombre = pedirNombre();
                if (nombres.includes(nombre)) {
                    alert("El nombre '" + nombre + "' ya ha sido agregado. No se puede repetir.");
                } else {
                    var calificaciones = pedirCalificaciones();
                    var promedio = calcularPromedio(calificaciones);
        
                    nombres.push(nombre);
                    promedios.push(promedio);
        
                    captura = confirm("¿Deseas capturar otro alumno?");
               }
            }
        
            alert("Adiós");
        
            // Mostrar nombres y promedios
            for (var i = 0; i < nombres.length; i++) {
                console.log("Nombre: " + nombres[i] + ", Promedio: " + promedios[i]);
            }
        }
        
        // Llamar a la función principal para iniciar el proceso
        capturarDatos();
## VERSION 8
Agregar resulatados al DOM

        // Función para pedir el nombre del alumno con validación usando length y toUpperCase
        function pedirNombre() {
            var nombre = "";
            while (!nombre || nombre.length < 3) {  // Validamos que el nombre tenga al menos 3 caracteres
                nombre = prompt("Ingresa el nombre del alumno (mínimo 3 caracteres)");
                if (!nombre || nombre.length < 3) {
                    alert("El nombre debe tener al menos 3 caracteres. Inténtalo de nuevo.");
                }
            }
            nombre = nombre.toUpperCase();  // Convertir el nombre a mayúsculas
            return nombre;
        }
        
        // Función para pedir las calificaciones de un alumno
        function pedirCalificaciones() {
            var calificaciones = [];
            for (var i = 0; i < 3; i++) {
                var calificacion = parseFloat(prompt("Ingresa la calificación " + (i + 1)));
                calificaciones.push(calificacion);
            }
            return calificaciones;
        }
        
        // Función para calcular el promedio de las calificaciones
        function calcularPromedio(calificaciones) {
            var suma = 0;
            for (var i = 0; i < calificaciones.length; i++) {
                suma += calificaciones[i];
            }
            var promedio = suma / calificaciones.length;
            return promedio;
        }
        
        // Función principal para capturar datos y mostrar resultados en el DOM
        function capturarDatos() {
            var nombres = [];
            var promedios = [];
            var captura = confirm("¿Deseas capturar un alumno?");
        
            while (captura) {
                var nombre = pedirNombre();
                if (nombres.includes(nombre)) {
                    alert("El nombre '" + nombre + "' ya ha sido agregado. No se puede repetir.");
                } else {
                    var calificaciones = pedirCalificaciones();
                    var promedio = calcularPromedio(calificaciones);
        
                    nombres.push(nombre);
                    promedios.push(promedio);
        
                    mostrarEnDom(nombre, promedio);
        
                    captura = confirm("¿Deseas capturar otro alumno?");
                }
            }
        
            alert("Adiós");
        }
        
        // Función para mostrar el nombre y promedio en el DOM
        function mostrarEnDom(nombre, promedio) {
            var listaAlumnos = document.getElementById("lista-alumnos");
            var li =    ("li");
            li.textContent = "Nombre: " + nombre + ", Promedio: " + promedio.toFixed(2);
            listaAlumnos.appendChild(li);
        }
        
        // Escuchar el clic del botón para iniciar la captura
        document.getElementById("capturar-btn").addEventListener("click", function() {
            capturarDatos();
        });


## VERSION 9

        document.getElementById("formulario").addEventListener("submit",function(){
            event.preventDefault();
            var nombre = document.getElementById("nombre").value.toUpperCase();
            var cal1 = parseFloat(document.getElementById("cal1").value);
            var cal2 = parseFloat(document.getElementById("cal2").value);
            var cal3 = parseFloat(document.getElementById("cal3").value);
        
            var calificaciones = [cal1,cal2,cal3];
        
            var promedio = calcularPromedio(calificaciones);
            mostrarEnDom(nombre,promedio); 
        
            document.getElementById("formulario").reset();
        }); 
        
        function calcularPromedio(calificaciones){
            var suma = 0;
            for(var i = 0; i < calificaciones.length;i++){
                suma = suma + calificaciones[i];
            }
            return suma / calificaciones.length;
        }
        
        function mostrarEnDom(nombre,promedio){
            var lista = document.getElementById("lista");
            var li = document.createElement("li");
            li.textContent = "Nombre: " + nombre + " Promedio: " + promedio;
            lista.appendChild(li);
        }   

html 

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Ejemplo DOM</title>
            <link rel="stylesheet" href="css/estilos.css">
        </head>
        <body>
            <h1>REGISTRO DE CALIFICACIONES</h1>
            <form id="formulario">
                Nombre: <input type="text" required id="nombre" name="nombre" maxlength="20" minlength="3">
                Calificacion 1: <input type="number" required id="cal1" min="0" max="10" step="0.1">
                Calificacion 2: <input type="number" required id="cal2" min="0" max="10" step="0.1">
                Calificacion 3: <input type="number" required id="cal3" min="0" max="10" step="0.1">
                <input type="submit" value="Registrar Alumno">
            </form>
        
            <h2>ALUMNOS REGISTRADOS</h2>
            <ol id="lista"></ol>
        
        
            <script src="js/main.js"></script>
        </body>
        </html>
        
css

        input[type="text"],[type="number"]{
            margin-bottom: 10px;
            display: block;
        }


# VERSION 10

JS

        class Alumno{
            constructor(nombre,apellido,cal1,cal2,cal3){
                this.nombre = nombre;
                this.apellido= apellido;
                this.cal1 = cal1;
                this.cal2 = cal2;
                this.cal3 = cal3;
                this.promedio = this.calcularPromedio();
                this.estatus = this.calcularEstatus();    
            }
            calcularPromedio(){
                return (this.cal1+this.cal2+this.cal3)/3;
            }
            calcularEstatus(){
                return this.promedio >= 6 ? "Aprobado":"Reprobado";
            }
            mostrarDatos(){
                return `
                Nombre: ${this.nombre}
                Apellido: ${this.apellido}
                Calificacoin1: ${this.cal1}
                Calificacion2: ${this.cal2}
                Calificacion3: ${this.cal2}
                Promedio: ${this.promedio}
                Estatus: ${this.estatus}`
            }
        }
        
        document.getElementById("formulario").addEventListener("submit", function(){
            event.preventDefault();
            const nombre = document.getElementById('nombre').value;
            const apellido = document.getElementById('apellido').value;
            const cal1 = parseFloat(document.getElementById('cal1').value);
            const cal2 = parseFloat(document.getElementById('cal2').value);
            const cal3 = parseFloat(document.getElementById('cal3').value);
        
            var alumno = new Alumno(nombre,apellido,cal1,cal2,cal3);
        
            document.getElementById('salida').textContent = `${alumno.mostrarDatos()}`;
        
        });





