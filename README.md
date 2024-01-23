<h1>Motor de recomendación 📚</h1>

<p>Éste proyecto es un challenge de FreeCodeCamp para modelos de Machine Leargnin de Clustering.<br>
Link del challenge.</p>

<h2>Importamos librerías y datos</h2>
<h2>Analizamos los datos</h2>
<p>Analizamos los datos importados y realizamos una búsqueda de anomalías como datos faltantes, errores tipográficos, etc.</p>
<h3>Analizamos el dataframe de libros</h3>
![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/3a70d468-8822-460f-ae2b-40200eb32cd8)

<p>Conclusión: No encontramos duplicados, ni nulos y tampoco anomalías en cuanto a la estructura y tipo de datos del dataframe</p>

<h3>Analizamos el dataframe de ratings</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/8ac3257a-2278-47d2-b728-2cd961fb1ece)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/b62b813d-e29c-4bec-a137-acf4ba78a090)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/94ffc8e3-806b-496b-9400-cfb3cc66ab31)

<p>Conclusión: No encontramos valores anómalos, negativos, en la columna user.</p>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/ce18da52-e406-4070-85bd-e92eccd36b30)

<p>Conclusión: No encontramos valores anómalos, negativos ni mayores a 10, en la columnas de rating.</p>

<h2>EDA: Análisis exploratorio de los datos</h2>

(insertar imagen aquí)

<p>Concluimos que hay información de libros que tienen muy pocas recomendaciones al igual que usuarios que recomendaron pocos libros. Vamos a limpiar estos datos para obtener información más significativa</p>

<h3>Eliminamos todos los libros que tengan menos de 100 calificaciones</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/95c5ac21-8383-41c2-9ed2-60bee7f66273)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/2c3ff604-ff2a-435a-9a11-77c388482aa9)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/7fe5f33f-d354-43a7-9ed4-1135b9b83a71)


<p>Como conclusión observamos que de 27.000 libros sólo 727 de ellos tenían suficientes calificaciones</p>

<h3>Eliminamos todos los usuarios que hayan hecho menos de 200 calificaciones</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/28d8cf74-563e-46c3-b071-8d707c738e9d)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/e741bb4a-6a06-459b-821b-92505870c77d)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/c225d992-ad08-4a2b-a995-490478326e7c)

<p>Después de la limpieza apreciamos que de 1.150.000 usuarios aproximadamente sólo 530.000 usuarios habían brindado 200 o más calificaciones</p>

<h2>Implementamos nuestro modelo de Machine Learning</h2>

Paso 1: armamos nuestra matriz de pivot <br>
Paso 2: Entrenamos nuestro modelo <br>
Paso 3: Creamos una función de recomendación para testear nuestro modelo

<h2>Testeamos nuestro modelo</h2>

<p>FreeCodeCamp nos brinda una función de test en donde para un libro específico buscado tenemos que obtener el siguiente resultado:</p>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/6d4f43b0-cdda-4c0a-9a08-c51ba0063b11)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/04a7e292-712f-476d-846d-6ce22d19468a)

<h3>Ejecutamos la función</h3>

<p>test_book_recommendation()</p>

<p>["Where the Heart Is (Oprah's Book Club (Paperback))", [["I'll Be Seeing You", 0.8], ['The Weight of Water', 0.77], ['The Surgeon', 0.77], ['I Know This Much Is True', 0.77], ['The Lovely Bones: A Novel', 0.72]]]
You passed the challenge! 🎉🎉🎉🎉🎉</p>


