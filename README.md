# Regresión Lineal con Machine Learning

```sh
from sklearn.model_selection import train_test_split
```

Si tienes datasets individuales, es decir para entrenamiento y otro para test no es necesario el código de arriba, de lo contrario si para evitar **Overfitting** o sobreajuste en los datos por lo que el modelo se ajustaría demasiado a los datos de entrenamiento y no puedría generalizar bien nuevos datos de predicción.

```sh
from sklearn.linear_model import LinearRegression
```
- Sklearn: Librería
- lineal_modelo: submódulo para trabajar modelos lineales
- LinearRegressión: Clase del submódulo, éste a su vez tiene los atributos coef_ que guarda los coeficientes para cada feature o variable de entrada con el que se multiplicará cada entrada, a su vez cuenta con intercept_ que guarda el coeficiente de intercepto o sesgo que se sumará a cada predicción.

después de actulizar esos variables con el método .fit puedes imprimir los coeficientes, ejemplo:

```sh
Entrenamiento
reg.fit(X_train, y_train)

Obtener los coeficientes y el término de intercepción
coeficientes = reg.coef_
intercepcion = reg.intercept_
```





