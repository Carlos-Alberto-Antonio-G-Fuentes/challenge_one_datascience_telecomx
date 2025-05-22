# challenge_one_datascience_telecomx
Challenge ONE Data Science – Telecom X
En este challenge se realizó lo siguiente:

1.   Se creo un DataFrame a partir del archivo JSON proporcionado denominado TelecomX_Data.
2.   Se reviso el contenido del DataFrame creado con el código datos.info().
3.   Se verificaron las columnas si contienen listas, con el código columnas=list(datos.columns).
4.   Se normalizaron las columnas que tenían listas (customer, phone, internet, account) y se expanden las columnas que contienen diccionarios y se crea un df llamado datos_normalizados.
5.   Se detecta otra columna con listas denominada Charges, la cual se normaliza y se procede a eliminar. De esta normalización se generan 2 nuevas columnas, denominadas MonthlyCharges y TotalCharges (esta información estaba contenida inicialmente como una lista en la columna Charges). Estas 2 columnas nuevas se unen a nuestro DataFrame datos_normalizados.
6.   Se crea un nuevo df denominado datos_final a partir de datos_normalizados.
7.   Se vuelve a revisar el contenido del DataFrame creado con el código datos_normalizados.info().
8.   Se procede a revisar si contienen datos vacios o Nan las columnas MonthlyCharges y TotalCharges, detectándose esta ocurrencia en la columna TotalCharges.
9.   Se reemplazan los datos vacíos por Nan.
10.  Se reemplazan los Nan por 0.0.
11.  Se verifica si quedaron Nan en la columna TotalCharges.
12.  Se convierte la columna TotalCharges a float64.
13.  Se vuelve a revisar el contenido del DataFrame creado con el código datos_final.info().
14.  Se revisa el diccionario.
15.  Se calculan las cuentas diarias y almacenando la información en una columna creada llamada Cuentas_Diarias.
16.  Se vuelve a revisar el contenido del DataFrame creado con el código datos_final.info().
17.  Se verifican las columnas que contienen valores Yes y NO.
18.  Estas columnas tenian valores distintos a YES o NO
Churn: ['No' 'Yes' ''] 
MultipleLines: ['No' 'Yes' 'No phone service'] 
OnlineSecurity: ['No' 'Yes' 'No internet service'] 
OnlineBackup: ['Yes' 'No' 'No internet service'] 
DeviceProtection: ['No' 'Yes' 'No internet service'] 
TechSupport: ['Yes' 'No' 'No internet service'] 
StreamingTV: ['Yes' 'No' 'No internet service'] 
StreamingMovies: ['No' 'Yes' 'No internet service']

Por lo anterior los valores distintos a YES o NO se reemplazaron por 0.
Además se detectó que la columna InternetService: ['DSL' 'Fiber optic' 'No'] si bien tiene valores NO, esta columna no será intervenida.

19.  Se cambian a minúscula las siguientes columnas:
gender
InternetService
Contract
PaymentMethod

21.  En la columna PaymentMethod, se reemplazan los siguientes valores:
credit card (automatic) por credit card automatic
bank transfer (automatic) por bank transfer automatic.

23.  En la columna Contract, se reemplazan los siguientes valores:
month-to-month por month to month

25.  Se revisa el archivo datos_final.
26.  Se calculan metricas con el codigo datos_final.describe().
27.  Se utiliza gráfico de torta (pie) para visualizar la proporción de clientes que permanecieron y los que se dieron de baja marcados en la columna Churn (1=activo;0=inactivo).
28.  Se crea un nuevo df denominado evasion, para analizar y graficar la evasión por genero, tipo de contrato y metodo de pago.
29.  Grafica evasion por genero, tipo de contrato y metodo de pago (cantidad de clientes).
30.  Grafica evasion por genero, tipo de contrato y metodo de pago (% de clientes).
31.  Se crea un nuevo df denominado evasion2, para analizar y graficar la evasión por TotalCharges y tenure.
32.  Grafico histograma para visualizar cómo se distribuyen las variables numéricas entre quienes cancelaron y quienes no, respecto TotalCharges y tenure.
