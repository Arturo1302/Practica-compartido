Algoritmo Registro_participante

Definir nombre, clasificacion como Caracter
Definir edad, nivel, shuttle como Entero

Escribir "Ingrese su nombre completo:"
Leer nombre

Escribir "Ingrese su edad:"
Leer edad   

Escribir "Ingrese el nivel (l) alcanzado: " 
Leer nivel

Escribir "Ingrese la cantidad de shuttle (s) alcanzados: "
Leer shuttle


velocidad <- 8 + 0.5 * nivel
VO2max <- 3.46 * velocidad + 12.2
VO2max_leger <- 31.025 + (3.238 * velocidad) - (3.248 * edad) + (0.1536 * velocidad * edad)
suma<- suma + VO2max
promedio_grupal <- suma / 10
suma2<- suma2 + VO2max_leger
promedio_grupal_leger <- suma2 / 10
   
---------------------------------------------------
     Para i=1 hasta 10 con paso 1 hacer
        Escribir "Ingrese su nombre completo:"
        Leer nombre

        Escribir "Ingrese su edad:"
        Leer edad   

        Escribir "Ingrese el nivel (l) alcanzado: " 
        Leer nivel

        Escribir "Ingrese la cantidad de shuttle (s) alcanzados: "
        Leer shuttle

            Mientras edad <= 0 hacer
                Escribir "Error, Ingrese una edad válida: "
                Leer edad
            FinMientras
            Mientras nivel <= 0 hacer
                Escribir "Error, Ingrese un nivel válido: "
                Leer nivel
            FinMientras
            Mientras shuttle < 0 hacer
                Escribir "Error, Ingrese una cantidad de shuttle válida: "
                Leer shuttle
            FinMientras

    FinPara     


 Si VO2max < 35 Entonces
            clasificacion <- "Baja"
        Sino
            Si VO2max >=35 o VO2max < 44.9 Entonces
                clasificacion <- "Promedio"
            Sino
                Si VO2max >= 45 o VO2max < 54.9 Entonces
                    clasificacion <- "Buena"
                Sino
                    Si VO2max >= 55  Entonces
                        clasificacion <- "Excelente"
                    FinSi
                FinSi
            FinSi
        FinSi

---------------------------------------------------
    Escribir "Nombre del participante: ", nombre
    Escribir "Edad: ", edad, "Años"
    Escribir "Nivel alcanzado: ", nivel
    Escribir "Cantidad de shuttle alcanzados: ", shuttle
    Escribir "Velocidad Final: ", velocidad, "Km/h"
    Escribir "VO2max Simple: ", VO2max, "ml/kg/min"
    Escribir "VO2max Leger: ", VO2max_leger, "ml/kg/min"
    Escribir "Clasificación. ", clasificacion
       
    Escribir "-------------------------------------"
    Escribir "Promedio grupal VO2max Simple: ", promedio_grupal, " ml/kg/min"
    Escribir "Promedio grupal VO2max Leger: ", promedio_grupal_leger, " ml/kg/min"
    