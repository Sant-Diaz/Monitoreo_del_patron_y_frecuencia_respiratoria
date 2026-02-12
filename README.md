<h1 align="center">Monitoreo Del Patron Y Frecuencia Respiratoria</h1>

##  ¿Qué es la frecuencia respiratoria?

La **frecuencia respiratoria (FR)** es el número de **ciclos completos de respiración (inspiración + espiración)** que realiza una persona por unidad de tiempo, normalmente expresado en **respiraciones por minuto (rpm)**. Se incluye como uno de los **signos vitales básicos** en medicina clínica y se utiliza para evaluar el estado respiratorio y general del paciente. (Nicolò A, Massaroni C, Schena E, Sacchetti M. The Importance of Respiratory Rate Monitoring)

> En términos fisiológicos:
>
> “La frecuencia respiratoria (es decir, el número de respiraciones por minuto) está altamente regulada para permitir que las células produzcan energía de forma óptima en función de las necesidades del organismo.” 
>
>  Sacado de: Chourpiliadis C, Bhardwaj A. Physiology, Respiratory Rate. Available from: [https://www.ncbi.nlm.nih.gov/books/NBK537306/?utm_source=chatgpt.com](https://www.ncbi.nlm.nih.gov/books/NBK537306/)


##  Fisiología de la respiración

### - El ciclo respiratorio

Una respiración completa consta de dos fases:  
1. **Inspiración** — entrada de aire a los pulmones  
2. **Espiración** — salida de aire hacia el ambiente
<div align="center">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQTxnPGqGmdluJs3qnf0VLcFsl0Ip6TxUlsOF0h-k7J8jiNOZ9hgAfyLL7BBCoiG3Av-KU&usqp=CAU" alt="Descripción" width="300">
</div>
Cada ciclo representa una única respiración.

### - Regulación nerviosa

La FR está controlada por centros en el **tronco cerebral**, específicamente en áreas como el **pre-Botzinger complex**, que generan un patrón rítmico para la respiración. Cuando los niveles de gases en sangre (por ejemplo CO₂) cambian, los quimiorreceptores ajustan la frecuencia y profundidad respiratoria. 

### - Rangos normales de frecuencia respiratoria

Los valores típicos en reposo varían según la edad y condición fisiológica:

<table align="center">
  <tr>
    <th>Grupo</th>
    <th>Frecuencia respiratoria normal</th>
  </tr>
  <tr>
    <td align="center">Recién nacido</td>
    <td align="center">~30–60 rpm</td>
  </tr>
  <tr>
    <td align="center">Infante</td>
    <td align="center">~30–60 rpm</td>
  </tr>
  <tr>
    <td align="center">Niño</td>
    <td align="center">~18–30 rpm</td>
  </tr>
  <tr>
    <td align="center">Adulto sano</td>
    <td align="center">~12–20 rpm</td>
  </tr>
  <tr>
    <td align="center">Adulto mayor</td>
    <td align="center">~12–28 rpm</td>
  </tr>
</table> 



##  Importancia clínica

La FR es uno de los **signos vitales más sensibles** que refleja el estado funcional del sistema respiratorio y la homeostasis general del organismo. Una variación significativa puede indicar condiciones como:

- **Hipoxia** (baja oxigenación)
- **Hipercapnia** (altos niveles de CO₂)
- **Insuficiencia respiratoria**
- **Deterioro clínico agudo** 

Además, su monitorización regular ayuda a detectar deterioros clínicos tempranos y a orientar decisiones médicas en unidades hospitalarias o de cuidados intensivos. :contentReference[oaicite:6]{index=6}



##  ¿Cómo se mide la frecuencia respiratoria hoy en día? – Estado del arte

###  1. Medición manual tradicional

El método clásico realizado por personal clínico consiste en:

- Observar el **movimiento torácico o abdominal**.
- Contar el número de respiraciones completas en **un minuto**. 

Este método es simple, pero presenta problemas de precisión, ya que depende del observador y puede verse afectado por la actividad del paciente, la distracción o la sospecha del paciente de ser observado. 

---

###  2. Métodos automatizados basados en sensores

Según revisiones académicas, los métodos tecnológicos para medir FR se dividen en varias categorías basadas en la variable fisiológica sensorizada: 

 - ***Flujo de aire:*** Los sensores neumotacográficos miden el flujo respiratorio mediante diferencias de presión causadas por el paso de aire durante la respiración. 

- ***Movimientos torácicos y abdominales:*** Sensores tipo *pneumograph* o sistemas de pletismografía miden cambios mecánicos de la pared corporal durante la respiración. 

- ***Modulación de señales cardíacas:*** Se puede extraer un componente respiratorio de señales como el ECG o el PPG y estimar la FR a partir de las variaciones periódicas inducidas por la respiración. 

- ***Métodos ópticos o sin contacto:*** Tecnologías como **remote photoplethysmography (rPPG)** o cámaras infrarrojas pueden estimar FR sin contacto físico directo con el paciente, aunque todavía son objeto de investigación activa. 

## Sensor y Montaje de Adquisición 
En este laboratorio se seleccionó el sensor MQ-3, un sensor activo, para la implementación de un sistema básico de capnografía, con el fin de estimar la concentración de CO₂ en el aire exhalado durante la respiración. Aunque el MQ-3 está diseñado para la detección de alcohol, su tecnología basada en óxido metálico semiconductor (MOS) permite detectar cambios en la composición de gases, incluyendo variaciones en la concentración de CO₂ presentes en el aliento. Por esta razón, puede emplearse como un indicador indirecto de CO₂, para lo cual se realizo una adecuada calibración del sensor y acondicionamiento de la señal.

El MQ-3 es un sensor activo porque requiere alimentación para su calentador interno, el cual eleva la temperatura del material sensible y permite que ocurran las reacciones químicas con los gases. Este calentamiento es lo que genera la variación de resistencia eléctrica que se mide como señal de salida.
<p align="center">
  <img src="https://naylampmechatronics.com/249-home_default/sensor-de-alcohol-mq3.jpg" height="220">
  <img src="https://naylampmechatronics.com/img/cms/Blog/Tutorial%20MQ/Estructura%20del%20sensor%20MQ.jpg" width="45%" height="220">
</p>
Se escogió este sensor por su bajo costo, rápido tiempo de respuesta, facilidad de integración con microcontroladores y disponibilidad comercial. En comparación con sensores de CO₂ por infrarrojo (NDIR), el MQ-3 representa una alternativa más simple y económica para fines académicos.

El montaje experimental se desarrollo con el controlador SP32, conectado al sensor MQ-3 que esta posicionado en una mascara de oxigeno adaptada para obtener una toma correcta de los datos, obtenidos mediante comunicacion serial.

