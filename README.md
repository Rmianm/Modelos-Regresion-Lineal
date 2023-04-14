# Regresión Lineal con Machine Learning

A continuación se explicara algunos códigos que se encuentran presentes en los archivos que he subido.

```sh
from sklearn.model_selection import train_test_split
```

Si tienes datasets individuales, es decir para entrenamiento y otro para test no es necesario el código de arriba, de lo contrario si para evitar **Overfitting** o sobreajuste en los datos por lo que el modelo se ajustaría demasiado a los datos de entrenamiento y no puedría generalizar bien nuevos datos de predicción.

Si tenemos un dataset con variables de entrada y el target debemos separar estas en dos variables diferentes, pueden ser X y Y. Para nuestros casos de regresión lineal lo haremos algo similar a lo siguiente:

variable = dataset.iloc[:,:1].values, el primer valor " : " quiere decir que va a tomar todas las filas, el segundo " :1" desde la columna con índice 0 hasta una antes que la columna con indice 1, es decir que para nuestro ejemplo solo estaría tomando la primer columna.

Hay una manera que tal vez te es más cómoda para una regresión lineal simple:
variable = dataset['feature'].values

Cuando has iniciado el entrenamiento debes dividir los datos en entrenamiento y test a partir de X y Y, recuerda que esto es si no tienes datasets individuales, puedes hacer así:

```sh
x_train, x_test, y_train, y_test = train_test_split(X,Y,test_size= 0.2, random_state= 0)
```
- test_size me define el porcentaje que utilizaré para entrenar, si eliges 0.2 es decir que el entrenamiento será el 80% y 30% para prueba.
- Random_state lo usamos por si queremos modificar el set de datos para entrenar, o queremos establecer una nueva semilla cada vez que ejecutemos el código; con 0 o cualquier otro numero entero fijo siempre tomaremos los mismos datos aleatorios (los guarda), es decir que si ejecuto de nuevo la linea estos datos permanecerán guardados y no se altera mi modelo, en cambio si establezo el valor de None, la semilla para la generación de números aleatorios se selecciona de forma aleatoria cada vez que se ejecuta el código. 

```sh
from sklearn.linear_model import LinearRegression
```
- Sklearn: Librería
- lineal_modelo: submódulo para trabajar modelos lineales
- LinearRegressión: Clase del submódulo, éste a su vez tiene los atributos coef_ que guarda los coeficientes para cada feature o variable de entrada con el que se multiplicará cada entrada, a su vez cuenta con intercept_ que guarda el coeficiente de intercepto o sesgo que se sumará a cada predicción.

después de actulizar esos variables con el método .fit puedes imprimir los coeficientes, ejemplo:

Entrenamiento
```sh
reg.fit(X_train, y_train)
```
Obtener los coeficientes y el término de intercepción

```sh
coeficientes = reg.coef_
intercepcion = reg.intercept_
```





