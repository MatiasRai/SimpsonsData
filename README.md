# Predicción DatasetSimpsons

# Proyecto de aprendizaje

En este proyecto desarrollaremos un clasificador de imágenes y video basado en Deep Learning utilizando el conjunto de datos de personajes de los Simpsons. La solución combina procesamiento de imágenes, redes neuronales CNN y una interfaz web interactiva mediante Gradio para facilitar la visualización y uso del modelo.

# ¿Qué haremos técnicamente?

**1. Carga y Preprocesamiento de Datos**  
   - Cargaremos el conjunto de datos.
   - Redimensionaremos y normalizaremos las imágenes.
   - Convertiremos las etiquetas a formato categórico (one-hot encoding).
   - Aplanaremos las imágenes para pasarlas a una red CNN.

**2. Construcción del Modelo**  
   - Diseñaremos una red neuronal CNN.
   - Usaremos capas densas con funciones de activación ReLU.
   - Añadiremos Dropout y regularización L2.
   - Finalizaremos con una capa `softmax` para clasificar las clases.

**3. Entrenamiento del Modelo**  
   - Compilaremos el modelo con optimizador SGD (con Nesterov), pérdida `categorical_crossentropy` y métrica `accuracy`.
   - Usaremos callbacks como `EarlyStopping`, `ModelCheckpoint`, `Learning rate scheduler` y `TensorBoard`.
   - Entrenaremos con validación y ajustaremos el learning rate dinámicamente.

**4. Evaluación y Métricas**  
   - Analizaremos el rendimiento del modelo con:
   - Matriz de confusión
   - Curvas de precisión y recall
   - Curvas ROC/AUC
   - Histogramas de desempeño por clase
   - Identificaremos las clases con mejor y peor desempeño.

**5. Interfaz Interactiva con Gradio**  
   - Implementaremos una interfaz web sencilla con Gradio.
   - Permitiremos al usuario cargar imágenes desde su dispositivo.
   - El modelo devolverá la clase predicha como salida textual.

# Requisitos previos
   - Google Colab: Acceso a una cuenta de Google y Google Colab.
   
   - Python 3.x: Si deseas ejecutar el proyecto localmente.
   
   - Internet: Para descargar el conjunto de datos de CIFAR-100 y los modelos.

# Instrucciones de uso 

   **Uso en Google Colab (Drive)**
   - **Accede a Google Colab:**

     -Abre Google Colab en tu navegador: https://colab.research.google.com.

   - **Carga el proyecto en Google Drive:**

     -Si no lo has hecho ya, sube tu repositorio a Google Drive.

     -Asegúrate de tener el repositorio guardado en una carpeta en Google Drive para poder accederlo fácilmente.

   - **Cargar el archivo dataset de los simpsons:**

     -El primer notebook requiere que descargues el archivo de los Simpsons.

     -Después de descargarlo, sube el archivo comprimido a tu Google Drive.

     -En el notebook, cambia las rutas de acceso al archivo para que apunten a la carpeta de Google Drive donde guardaste el archivo del dataset de los Simpsons.

   - **Ejecutar el Notebook:**

     -En el notebook de Google Colab, ejecuta todas las celdas para cargar los datos, preprocesarlos, construir y entrenar el modelo.

     -Si todo está configurado correctamente, el modelo se entrenará y podrás visualizar los resultados de la clasificación.

   - **Guardar los resultados:**

     -Puedes guardar el modelo entrenado en Google Drive, o también puedes descargarlo para usarlo en un entorno local si lo prefieres.

   - **Cargar los datos localmente:**

      -Cambia las rutas de acceso en el notebook de Colab para que apunten a la ubicación donde subiste el archivo en Colab.

     -Asegúrate de descomprimir el archivo antes de cargar los datos.

   - **Ejecutar el notebook:**

     -Ejecuta las celdas en orden dentro de Google Colab. Esto cargará los datos, los preprocesará y entrenará el modelo.

   **Uso del Modelo Preentrenado**
     
   - **Descargar el Modelo:**

     -Si prefieres utilizar un modelo preentrenado, puedes descargarlo desde el repositorio del proyecto o desde algún enlace proporcionado en la documentación.

     -Asegúrate de que la ruta del modelo esté correctamente configurada en el código.

   - **Cambiar las Rutas:**

     -Asegúrate de cambiar las rutas a las de tu archivo local o en Google Drive.

     -La ruta debe ser actualizada dentro de los notebooks para que apunten a la ubicación donde descargaste el modelo.

   - **Cargar el Modelo:**

     -Una vez configurada la ruta, ejecuta el código para cargar el modelo preentrenado y realizar la validación en los datos del dataset de los Simpsons.

# Ventajas de usar gradio

- Fácil de compartir: El enlace público permite compartir con cualquier persona.
- Feedback visual: Muestra las probabilidades de las principales predicciones.
- Interfaz amigable: Permite a las personas interactuar con el modelo sin la necesidad de escribir código.

# Conclusión

**1. Rendimiento General:**

   El modelo CNN logra un buen rendimiento para de identificación de personajes para los Simpsons.

**2. Limitaciones:**
   - El modelo puede tener dificultades con objetos rotados o en diferentes posiciones.
   -El modelo tiene overfitting.

**3. Mejoras Potenciales:**
   - Probar arquitecturas más complejas (más capas, más unidades).
   - Implementar técnicas de aumentación de datos (rotaciones, volteos, zoom).
   - Ajustar los hiperparámetros mediante búsqueda de cuadrícula o aleatoria.


# Documentación y enlaces útiles
  
- [Documentación de Keras](https://keras.io/api/optimizers/)
