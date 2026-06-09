# Riesgo Crediticio - Machine Learning Engineering (DSRP) 🚀

## a. Problema de ML
El objetivo de este proyecto es resolver un problema de **Clasificación Supervisada**. Buscamos predecir si un cliente caerá en incumplimiento de pago (Default) o no (No Default) basándonos en su historial y características financieras.

## b. Descripción del Dataset
El conjunto de datos contiene información financiera de clientes.
* `person_age`: Edad de la persona.
* `person_income`: Ingreso anual.
* `loan_amnt`: Monto del préstamo solicitado.
* `loan_status`: Variable objetivo (0 = No Default, 1 = Default).

## c. Model Card
* **Modelo utilizado:** Random Forest Classifier (Bosque Aleatorio).
* **Parámetros:** `n_estimators=100`, `random_state=42`.
* **Ventajas:** Robusto ante outliers y excelente para capturar relaciones no lineales en perfiles financieros.

## d. Resultados y Métricas
* **Métrica elegida:** Accuracy 
* **Accuracy obtenido:** *93%*.

## e. Conclusiones de Negocio (Generadas por IA)

**CONCLUSIÓN** 

Hemos finalizado el entrenamiento de un modelo de Machine Learning diseñado para predecir el riesgo crediticio, es decir, identificar si un cliente es propenso a caer en *default* o no. En general, el modelo es bastante robusto y **acierta en sus predicciones el 93% de las veces**. Es particularmente fuerte al identificar clientes que *no* representarán un riesgo: de los clientes que efectivamente no incumplieron, el modelo los identificó correctamente en un 99% de las ocasiones. Esto es excelente para agilizar aprobaciones de crédito de bajo riesgo con alta confianza.

Sin embargo, al analizar más a fondo los casos de riesgo, observamos un aspecto importante. Cuando el modelo predice que un cliente *sí* va a caer en *default*, tiene una precisión muy alta del 96%, lo que significa que rara vez nos da una "falsa alarma" sobre un cliente de alto riesgo. La principal área de oportunidad reside en su capacidad para *detectar a todos* los clientes que realmente van a incumplir: actualmente, **el modelo identifica correctamente al 71% de los clientes que finalmente caen en default**.

Esto implica que aproximadamente el 29% de los clientes que eventualmente incumplirían sus pagos no están siendo identificados como de alto riesgo por el modelo. En resumen, tenemos una herramienta muy potente para validar a los clientes de bajo riesgo y una alta confianza en los que el modelo señala como de alto riesgo. Nuestro siguiente paso será enfocar esfuerzos en mejorar la capacidad del modelo para "atrapar" a esa porción de clientes que, aunque terminen en *default*, el modelo no logra identificar a tiempo.*.