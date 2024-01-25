<h1>Motor de recomendaciones 📚</h1>

> [!NOTE]
> Éste proyecto es un challenge de FreeCodeCamp para modelos de <b>Machine Leargnin</b> de <b>Clustering</b>. <br>
> Desarrollado con mucho amor :love_letter: como aporte a la comunidad de científico de datos ya que <br>
> a la fecha se encuentra muy poca documentación sobre éste challenge en particular.

> [!CAUTION]
> Utilizar con fines educativos :octocat:


<h2>Stack de tecnologías</h2>

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)




<h2>Analizamos los datos</h2>
<p>Analizamos los datos importados y realizamos una búsqueda de anomalías como datos faltantes, errores tipográficos, etc.</p>
<h3>Analizamos el dataframe de libros</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/3a70d468-8822-460f-ae2b-40200eb32cd8)

- [x] <b>Conclusión:</b> No encontramos duplicados, ni nulos y tampoco anomalías en cuanto a la estructura y tipo de datos del dataframe

<h3>Analizamos el dataframe de ratings</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/8ac3257a-2278-47d2-b728-2cd961fb1ece)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/b62b813d-e29c-4bec-a137-acf4ba78a090)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/94ffc8e3-806b-496b-9400-cfb3cc66ab31)

- [x] <b>Conclusión:</b> No encontramos valores anómalos, negativos, en la columna user.

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/ce18da52-e406-4070-85bd-e92eccd36b30)

- [x] <b>Conclusión:</b> No encontramos valores anómalos, negativos ni mayores a 10, en la columnas de rating.

<h2>EDA: Análisis exploratorio de los datos</h2>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/4153671d-0bf2-4e4e-9548-00c3c71800e5)

> [!WARNING]
> Encontramos que hay información de libros que tienen muy pocas recomendaciones al igual que usuarios que recomendaron pocos libros.
> Vamos a limpiar estos datos para obtener información más significativa.

<h3>Eliminamos todos los libros que tengan menos de 100 calificaciones</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/95c5ac21-8383-41c2-9ed2-60bee7f66273)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/2c3ff604-ff2a-435a-9a11-77c388482aa9)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/7fe5f33f-d354-43a7-9ed4-1135b9b83a71)


- [x] <b>Conclusión:</b> observamos que de 27.000 libros sólo 727 de ellos tenían suficientes calificaciones

<h3>Eliminamos todos los usuarios que hayan hecho menos de 200 calificaciones</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/28d8cf74-563e-46c3-b071-8d707c738e9d)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/e741bb4a-6a06-459b-821b-92505870c77d)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/c225d992-ad08-4a2b-a995-490478326e7c)

<p>Después de la limpieza apreciamos que de 1.150.000 usuarios aproximadamente sólo 530.000 usuarios habían brindado 200 o más calificaciones</p>

<h2>Implementamos nuestro modelo de Machine Learning</h2>

<h3>Armamos una matriz de pivot</h3>

<p>Esta matriz de pivot representa por cada libro (filas) qué usuarios (columnas) dieron una puntuación y de cuánto fué la puntuación (valor)</p>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/1ea75f48-7fa5-4cc4-b6a9-9fd9b95eaf3c)

<h3>Entrenamos nuestro modelo de Machine Learning</h3>

<p>El modelo entrenado es KNN</p>

<h3> Creamos la función de recomendación </h3>

<table><tr><td> > def <b>test_book_recommendation(</b> book_name: string <b>)</b> -> list </td></tr></table>

<h3>Ejecutamos la fucnión de recomendación</h3>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/7889f3be-08fc-4caf-86af-7348b967c166)


<h2>Testeamos nuestro modelo</h2>

<p>FreeCodeCamp nos brinda una función de test en donde para un libro específico buscado tenemos que obtener el siguiente resultado:</p>

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/6d4f43b0-cdda-4c0a-9a08-c51ba0063b11)

![image](https://github.com/pabloing93/book-recommendations-engine/assets/32267303/04a7e292-712f-476d-846d-6ce22d19468a)

<h3>Ejecutamos la función de TEST</h3>

<table><tr><td> > test_book_recommendation()</td></tr></table>

<h3>Resultado</h3>

<table><tr><td> > ["Where the Heart Is (Oprah's Book Club (Paperback))", [["I'll Be Seeing You", 0.8], ['The Weight of Water', 0.77], ['The Surgeon', 0.77], ['I Know This Much Is True', 0.77], ['The Lovely Bones: A Novel', 0.72]]] </td></tr></table>

<table><tr><td> > You passed the challenge! 🎉🎉🎉🎉🎉</td></tr></table>

[Link al código](https://github.com/pabloing93/book-recommendations-engine/blob/main/book_recommendation.ipynb)

