# PROYECTO-3-PYTHON-KATAS
PROYECTO 3: PYTHON
Katas de Lógica, Funciones, POO y Manejo de Excepciones 
Este proyecto reúne un conjunto de 40 katas de Python orientadas al aprendizaje progresivo del lenguaje, desde un nivel básico hasta un nivel intermedio. Su finalidad es consolidar los fundamentos de programación mediante ejercicios de lógica, uso de funciones, programación funcional con map(), filter() y reduce (), recursividad, tratamiento de excepciones, entrada por teclado y programación orientada a objetos.
El trabajo principal está desarrollado en el notebook Proyecto 3. ipynb, que contiene los enunciados, las soluciones implementadas y distintos ejemplos de ejecución.
________________________________________
Tabla de contenidos
1.	Descripción del proyecto
2.	Contenido trabajado
3.	Estructura actual del proyecto
4.	Stack y compatibilidad
5.	Guía de ejecución
6.	Qué se aprende con el proyecto
7.	Resultados y ejemplos
8.	Buenas prácticas y estilo Python
9.	Limitaciones actuales y mejoras futuras
10.	Roadmap / Próximos pasos
11.	Autor
________________________________________
1. Descripción del proyecto
A lo largo del proyecto se trabajan ejercicios diseñados para practicar los principales bloques de introducción a Python:
•	funciones con y sin parámetros;
•	valores por defecto;
•	listas, tuplas y diccionarios;
•	programación funcional con map(), filter() y reduce ();
•	funciones lambda;
•	recursividad;
•	estructuras condicionales con if, elif y else;
•	manejo de excepciones con try y except;
•	entrada de datos mediante input ();
•	clases y objetos;
•	procesamiento de texto;
•	validación de datos;
•	problemas algorítmicos sencillos.
Los ejercicios incluyen tareas como contar frecuencias de letras en una cadena, calcular medias y clasificaciones, filtrar listas con condiciones, convertir listas de dígitos en números, detectar duplicados, enmascarar cadenas, buscar empleados en estructuras de datos y trabajar con clases como Arbol y UsuarioBanco.
Se trata de un proyecto útil para afianzar la lógica de programación y ganar soltura con la sintaxis de Python antes de afrontar desarrollos más grandes o estructurados.
________________________________________
2. Contenido trabajado
El notebook aborda ejercicios de distintas familias:
Funciones y estructuras básicas
Se incluyen ejercicios de conteo, búsqueda, cálculo de medias, operaciones con listas y manipulación de cadenas.
Programación funcional
Una parte importante del trabajo se centra en el uso de:
•	map() para transformar datos,
•	filter() para seleccionar elementos,
•	reduce() para acumular resultados,
•	y expresiones lambda para definir funciones sencillas de forma compacta.
Recursividad
Se trabaja la recursividad con el cálculo del factorial, lo que permite comprender el caso base y la llamada recursiva.
Excepciones y validación
Varios ejercicios se centran en validar entradas del usuario y manejar errores, por ejemplo, al dividir por cero, introducir valores no numéricos o trabajar con listas vacías.
Programación orientada a objetos
Se implementan las clases Arbol y UsuarioBanco, con sus respectivos atributos y métodos para practicar encapsulación y lógica interna.
Procesamiento de texto
También se incluyen tareas de conteo de palabras, reemplazo, eliminación y búsqueda de cadenas dentro de textos y listas.
________________________________________
3. Estructura actual del proyecto
En su estado actual, el proyecto está organizado de forma sencilla y gira en torno al notebook principal:
Proyecto_3_Python/
├─ Proyecto 3. ipynb
└─ README.md
________________________________________
4. Stack y compatibilidad
•	Lenguaje principal: Python 3
•	Entorno recomendado: Jupyter Notebook, VS Code, PyCharm o Google Colab
•	Librerías utilizadas: librerías estándar de Python, principalmente:
o	functools
o	operator
No se requieren dependencias externas para ejecutar el notebook.
________________________________________
5. Guía de ejecución
Opción principal: ejecutar el notebook
La forma natural de usar este proyecto es abrir el archivo Proyecto 3. ipynb en Jupyter Notebook, JupyterLab, VS Code o Google Colab y ejecutar las celdas en orden.
Recomendación de uso
Dado que varios ejercicios dependen de definiciones previas y algunos utilizan input(), lo más recomendable es:
1.	ejecutar el notebook de arriba abajo;
2.	revisar cada ejercicio junto con su salida;
3.	probar variantes manuales cuando el ejercicio lo permita.
Organización por bloques
Los ejercicios pueden entenderse también por bloques temáticos:
•	Funciones y estructuras básicas: 1–7, 12, 14, 16, 25, 27
•	Programación funcional (map, filter, reduce, lambda): 2, 4, 7, 9, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 26, 33
•	Excepciones y validación: 8, 10, 11, 31, 41
•	Recursividad y algoritmia: 6, 17, 28, 29, 30
•	POO / clases y objetos: 34 y 36
•	Procesamiento de texto: 1, 3, 12, 16, 29, 30, 37
•	Condicionales y lógica aplicada: 38, 39, 40 y 41
________________________________________
6. Qué se aprende con el proyecto
Este proyecto permite desarrollar competencias muy importantes en Python:
•	descomponer problemas en funciones pequeñas y reutilizables;
•	usar correctamente listas, diccionarios y tuplas;
•	aplicar map(), filter() y reduce() en casos reales;
•	comprender la diferencia entre print() y return;
•	trabajar con recursividad;
•	manejar excepciones para evitar fallos del programa;
•	validar entradas de usuario;
•	organizar clases y métodos con lógica sencilla;
•	procesar texto y colecciones de forma eficiente;
•	mejorar la legibilidad y mantenibilidad del código.
________________________________________
7. Resultados y ejemplos
A continuación, se recogen algunos ejemplos representativos del tipo de ejercicios trabajados en el notebook.
1) Frecuencia de letras en una cadena
def frecuencia_letras(cadena):
    conteo = {}
    for letra in cadena:
        if letra!= " ":
            conteo[letra] = conteo.get(letra, 0) + 1
    return conteo

print(frecuencia_letras("hola mundo"))
Salida esperada:
{'h': 1, 'o': 2, 'l': 1, 'a': 1, 'm': 1, 'u': 1, 'n': 1, 'd': 1}
________________________________________
2) Factorial recursivo
def factorial_recursivo(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial_recursivo(n - 1)

print(factorial_recursivo(5))
Salida esperada:
120
________________________________________
3) Filtrado de estudiantes con nota alta
estudiantes = [
    {"nombre": "Ana", "edad": 20, "calificacion": 95},
    {"nombre": "Luis", "edad": 21, "calificacion": 82},
    {"nombre": "Marta", "edad": 22, "calificacion": 91}
]

destacados = list(filter(lambda e: e["calificacion"] >= 90, estudiantes))
print(destacados)
Salida esperada:
[
    {'nombre': 'Ana', 'edad': 20, 'calificacion': 95},
    {'nombre': 'Marta', 'edad': 22, 'calificacion': 91}
]
________________________________________
4) Clase Arbol
arbol = Arbol()
arbol.crecer_tronco()
arbol.nueva_rama()
arbol.crecer_ramas()
print(arbol.info_arbol())
Salida esperada:
{
    'longitud_tronco': 2,
    'numero_ramas': 1,
    'longitudes_ramas': [2]
}
________________________________________
5) Clase UsuarioBanco
alicia = UsuarioBanco("Alicia", 100, True)
bob = UsuarioBanco("Bob", 50, True)

bob.agregar_dinero(20)
alicia.transferir_dinero(bob, 80)
alicia.retirar_dinero(50)

print(alicia.nombre, alicia.saldo)
print(bob.nombre, bob.saldo)
________________________________________
6) Procesamiento de texto con varias opciones
def contar_palabras(texto):
    palabras = texto.split()
    diccionario = {}

    for palabra in palabras:
        if palabra in diccionario:
            diccionario[palabra] += 1
        else:
            diccionario[palabra] = 1
    return diccionario
Este bloque se completa con funciones para reemplazar o eliminar palabras y una función principal procesar_texto() que decide qué operación ejecutar según la opción elegida.
________________________________________
8. Buenas prácticas y estilo Python
Durante el proyecto se han ido consolidando varias buenas prácticas:
•	usar nombres de funciones y variables descriptivos;
•	mantener la indentación de 4 espacios;
•	no reutilizar nombres de variables con significados distintos;
•	separar la lógica del cálculo de la interacción con el usuario;
•	usar return cuando una función debe devolver un resultado;
•	validar siempre entradas sensibles;
•	documentar ejercicios con comentarios breves cuando sea útil;
•	intentar seguir las recomendaciones de estilo de PEP 8.
________________________________________
9. Limitaciones actuales y mejoras futuras
En su estado actual, el proyecto funciona bien como cuaderno formativo, pero todavía puede mejorarse en varios aspectos:
•	algunas soluciones podrían ajustarse con más precisión al enunciado;
•	varios ejercicios interactivos con input() podrían refinarse para ser más reutilizables;
•	sería conveniente asegurar una ejecución limpia del notebook desde un kernel reiniciado;
•	faltaría modularizar el código en archivos .py separados;
•	aún no se han incorporado pruebas automatizadas reales.
________________________________________
10. Roadmap / Próximos pasos
Las siguientes mejoras serían especialmente recomendables:
1.	revisar y pulir los ejercicios más interactivos;
2.	unificar estilo de nombres y estructura de funciones;
3.	extraer las katas del notebook a módulos .py por bloques temáticos;
4.	añadir docstrings a las funciones principales;
5.	incorporar pruebas unitarias con unittest o pytest;
6.	añadir tipado estático con type hints;
7.	crear una versión del proyecto con menú interactivo o ejecución por bloques.
________________________________________
11. Autor
Pablo Chico Merino

