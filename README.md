# Regresión Lineal con Machine Learning


```sh
from sklearn.linear_model import LinearRegression
```
Sklearn: Librería
lineal_modelo: submódulo para trabajar modelos lineales
LinearRegressión: Clase del submódulo, éste a su vez tiene los atributos coef_ que guarda los coeficientes para cada feature o variable de decisión con el que se multiplicará cada entrada, a su vez cuenta con intercept_ que guarda el coeficiente de intercepto o sesgo que se sumará a cada predicción.

después de actulizar esos variables con el método .fit puedes imprimir los coeficientes, ejemplo:

```sh
Entrenamiento
reg.fit(X_train, y_train)

Obtener los coeficientes y el término de intercepción
coeficientes = reg.coef_
intercepcion = reg.intercept_
```





