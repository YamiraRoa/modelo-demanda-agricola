# Optimización de proyeccion de demanda en la industria agrícola

## Descripción
Este proyecto tiene como objetivo mejorar la precisión de las proyecciones de demanda en la industria agrícola mediante el uso del modelo SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous factors). La industria agrícola enfrenta retos importantes debido a la variabilidad estacional y a factores externos que afectan la demanda, lo que puede llevar a un exceso de inventario, costos de almacenamiento innecesarios y una inmovilización de capital. La implementación de este modelo permite optimizar la toma de decisiones en cuanto a inventarios y gestión de recursos.

## Configuración de ambiente local

Todas las pruebas en local fueron realizadas utilizando **Visual Studio Code (VSCode)**, por lo que se recomienda su uso para facilitar la configuración y ejecución del proyecto.

### Requisitos previos:

Se asume que Python está instalado a través de **Anaconda**. Si no tienes Anaconda instalado, puedes descargarlo desde [este enlace](https://www.anaconda.com/download).

### Pasos para configurar el entorno:

1. **Clonar el repositorio:**

   Clona este repositorio en tu máquina local utilizando el siguiente comando:
   ```bash
   git clone https://github.com/YamiraRoa/modelo-demanda-agricola
   cd tu-repo
   ```
   o utilizando la UI de vscode.
2. **Crear un ambiente virtual:**

    Se recomienda crear un ambiente virtual para aislar las dependencias del proyecto. Puedes hacerlo de la siguiente manera:
    ```bash
    En sistemas Unix/macOS:
    python -m venv venv
    source venv/bin/activate
    ```
    En sistema Windows:
    ```bash
    python -m venv venv
    .\venv\Scripts\activate
    ```
3. **Instalar las dependencias del proyecto:**

   Con el ambiente virtual activado, instala las dependencias del proyecto con el siguiente comando:
   ```bash
   pip install -r requirements.txt
   ```
## Descripción del Notebook

El notebook [`modelo_de_demanda.ipynb`](./modelo_de_demanda.ipynb) está dividido en las siguientes secciones principales:

1. *Carga de Datos*:
   - En esta sección, se cargan los datos históricos de ventas y precios en un formato CSV. Asegúrate de proporcionar la ruta correcta a tu archivo de datos.
   
2. *Análisis Exploratorio de Datos*:
   - Se realiza un análisis preliminar de los datos, incluyendo visualizaciones de las series temporales de ventas y precios.
   
3. *Preparación de los Datos*:
   - Los datos se procesan para asegurarse de que estén en el formato correcto para ser utilizados en el modelo ARIMA. Esto incluye convertir la columna de fechas y manejar los datos faltantes (si es necesario).

4. *Modelado SARIMAx*:
   - Se implementa el modelo SARIMAX utilizando la librería statsmodels. Aquí puedes ajustar los parámetros del modelo para mejorar las predicciones según tu dataset.

5. *Evaluación y Visualización de Resultados*:
   - Una vez entrenado el modelo, se visualizan las predicciones y se comparan con los datos reales para evaluar el rendimiento.

## Ejecución del Notebook

1. *Asegúrate de tener las dependencias instaladas*:
   - Sigue los pasos para instalar las librerías desde [`requirements.txt`](./requirements.txt).
   
2. *Modifica la ruta del archivo de datos*:
   - En la primera celda del notebook, encontrarás una variable para la ruta del archivo CSV. Asegúrate de modificar esta ruta para que apunte a tus datos locales.

3. *Ejecuta cada celda en secuencia*:
   - Puedes ejecutar cada celda del notebook de manera secuencial, desde la carga de los datos hasta la visualización de resultados. Se recomienda ejecutar las celdas paso a paso para garantizar que todo esté funcionando correctamente.

4. **Ajustes en el modelo SARIMAX**:
   - Si deseas ajustar el modelo SARIMAX (por ejemplo, cambiar los parámetros p, d, q, P, D, Q, s o agregar variables exógenas), puedes hacerlo en la sección correspondiente del notebook. Se incluyen comentarios en el código para guiarte en este proceso.

## Detalles Técnicos

### Librerías Utilizadas

- pandas para la manipulación de datos
- numpy para cálculos numéricos
- statsmodels para el modelado ARIMA
- pmdarima para la automatización del modelado ARIMA
- matplotlib y seaborn para la visualización de datos
- jupyter para la ejecución interactiva del notebook

Verifica las versiones exactas en el archivo [`requirements.txt`](./requirements.txt) y accede a la documentación de cada una de estas librerías:

- [pandas](https://pandas.pydata.org/pandas-docs/stable/)
- [numpy](https://numpy.org/doc/)
- [statsmodels](https://www.statsmodels.org/stable/)
- [pmdarima](http://alkaline-ml.com/pmdarima/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [jupyter](https://jupyter.org/documentation)

### Versión de Python Recomendado

Este proyecto ha sido probado en Python 3.11, aunque algunas versiones anteriores y superiores deberían ser compatibles.

## Licencia y Restricciones de Uso

Este proyecto está bajo la licencia MIT. Puedes revisar el archivo [`LICENSE`](./LICENSE) para más detalles.



