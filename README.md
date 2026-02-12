<h1 align="center">Monitoreo Del Patron Y Frecuencia Respiratoria</h1>
<div style="text-align: justify;">
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

###  2. Métodos automatizados basados en sensores

Según revisiones académicas, los métodos tecnológicos para medir FR se dividen en varias categorías basadas en la variable fisiológica sensorizada: 

 - ***Flujo de aire:*** Los sensores neumotacográficos miden el flujo respiratorio mediante diferencias de presión causadas por el paso de aire durante la respiración. 

- ***Movimientos torácicos y abdominales:*** Sensores tipo *pneumograph* o sistemas de pletismografía miden cambios mecánicos de la pared corporal durante la respiración. 

- ***Modulación de señales cardíacas:*** Se puede extraer un componente respiratorio de señales como el ECG o el PPG y estimar la FR a partir de las variaciones periódicas inducidas por la respiración. 

- ***Métodos ópticos o sin contacto:*** Tecnologías como **remote photoplethysmography (rPPG)** o cámaras infrarrojas pueden estimar FR sin contacto físico directo con el paciente, aunque todavía son objeto de investigación activa. 

## Sensor y Montaje de Adquisición 
En este laboratorio se seleccionó el sensor MQ-3, un sensor activo, para la implementación de un sistema básico de capnografía, con el fin de estimar la concentración de CO₂ en el aire exhalado durante la respiración. Aunque el MQ-3 está diseñado para la detección de alcohol, su tecnología basada en óxido metálico semiconductor (MOS) permite detectar cambios en la composición de gases, incluyendo variaciones en la concentración de CO₂ presentes en el aliento. Por esta razón, puede emplearse como un indicador indirecto de CO₂, para lo cual se realizo una adecuada calibración del sensor y acondicionamiento de la señal. El MQ-3 es un sensor activo porque requiere alimentación para su calentador interno, el cual eleva la temperatura del material sensible y permite que ocurran las reacciones químicas con los gases. Este calentamiento es lo que genera la variación de resistencia eléctrica que se mide como señal de salida.
<p align="center">
  <img src="https://naylampmechatronics.com/249-home_default/sensor-de-alcohol-mq3.jpg" height="220">
  <img src="https://naylampmechatronics.com/img/cms/Blog/Tutorial%20MQ/Estructura%20del%20sensor%20MQ.jpg" width="30%" height="220">
</p>

El montaje experimental se desarrollo con el controlador SP32, conectado al sensor MQ-3 que esta posicionado en una mascara de oxigeno adaptada para obtener una toma correcta de los datos, obtenidos mediante comunicacion serial.
<table align="center">
  <tr>
    <td align="center">
      <img src="https://docs.sunfounder.com/projects/umsk/en/latest/_images/Lesson_04_MQ2_Module_esp32_bb.png" height="220" style="object-fit: contain;">
    </td>
    <td align="center">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQzXk6oAroRoYw_BMhe7DcQxZ2iMPhXdyAHDA&s" height="220" style="object-fit: contain;">
    </td>
  </tr>
</table>

## Adquisición de la Señal 
El codigo utilizado para que la SP32 capture los datos adquiridos por el sensor MQ-3 es el siguiente:
```
const int potPin = 34;  // P34 (ADC1)
void setup() {
  Serial.begin(115200);
  delay(100);

  analogReadResolution(12);      // 0..4095
  analogSetAttenuation(ADC_11db); // rango aprox hasta ~3.3V
}

void loop() {
  int adc = analogRead(potPin);                 // 0..4095
  float v = (adc / 4095.0) * 5.0;               // voltaje estimado 0..3.3V

  // Formato: adc,voltaje  (para que MATLAB lo lea fácil)
  Serial.print(adc);
  Serial.print(",");
  Serial.println(v, 3);

  delay(100);
}
```
Posteriormente se realizo un codigo en MATLAB para la adqusicion de la señal y postprocesamiento de la misma. El cual se subdividio en las siguientes 10 secciones:
### 1. Configuración 
```
port = "COM11";
baud = 115200;
Ts_plot = 0.05;
W = 15;
```
Define el puerto de comunicación (COM11), la velocidad de transmisión (baud), la tasa de actualización de la gráfica y el tamaño de la ventana para el promedio móvil. Estos parámetros permiten adaptar el sistema al hardware y controlar la estabilidad de la señal.
### 2. Interfaz gráfica
```
figUI = figure("Name","Adquisición ESP32","Color","w", ...
    "Position",[500 300 420 250], "MenuBar","none", ...
    "NumberTitle","off", "Resize","off");

uicontrol(figUI,"Style","text","Position",[40 170 340 30], ...
    "String","Digite el tiempo en segundos para tomar la señal", ...
    "BackgroundColor","w");

editTime = uicontrol(figUI,"Style","edit","Position",[140 135 140 30], ...
    "String","60");

uicontrol(figUI,"Style","pushbutton","Position",[130 70 160 40], ...
    "String","INICIAR","Callback",@startAcquisition);

handles.editTime = editTime;
handles.port = port;
handles.baud = baud;
handles.Ts_plot = Ts_plot;
handles.W = W;
guidata(figUI, handles);
```
Crea una ventana donde el usuario ingresa el tiempo de adquisición. Utiliza controles *uicontrol* para recibir el valor y un botón que activa la función de adquisición.

### 3. Comunicación Serial
```
function startAcquisition(src,~)

handles = guidata(src);
T = str2double(handles.editTime.String);

if isnan(T) || T<=10
    errordlg("Ingrese un tiempo válido (>=10s).");
    return;
end

s = serialport(handles.port, handles.baud);
configureTerminator(s,"LF"); flush(s);

t0 = tic; t = []; v = []; v_f = []; lastPlot = 0;

figPlot = figure("Name","Voltaje - ESP32","Color","w");
h = animatedline('LineWidth',1.5);
xlabel("Tiempo (s)"); ylabel("Voltaje (V)");
grid on; ylim([0 5]); xlim([0 T]);
```
Inicializa el puerto serial con *serialport* para recibir datos desde el ESP32. Cada línea recibida corresponde a una muestra de voltaje del sensor MQ-3.

### 4. Adquisición en Tiempo Real 
```
while toc(t0) < T && isvalid(figPlot)

    line = strtrim(readline(s));
    val = str2double(split(line,","));

    if isfinite(val(end))

        ti = toc(t0);
        t(end+1,1) = ti;
        v(end+1,1) = val(end);

        if numel(v) < handles.W
            vf = mean(v);
        else
            vf = mean(v(end-handles.W+1:end));
        end

        v_f(end+1,1) = vf;

        if (ti-lastPlot) >= handles.Ts_plot
            addpoints(h,ti,vf);
            drawnow limitrate;
            lastPlot = ti;
        end
    end
end
clear s;
```
Lee continuamente los datos, calcula un promedio móvil para suavizar el ruido y los grafica en tiempo real usando *animatedline*. Esto permite observar el comportamiento respiratorio durante la medición.
### 5. Detección de Respiraciones
```
[pks_raw, locs_raw] = findpeaks(v_f,t,'MinPeakProminence',0.05);

Tmin = 3;
locs=[]; pks=[];
for k=1:length(locs_raw)
    if isempty(locs) || (locs_raw(k)-locs(end))>=Tmin
        locs(end+1)=locs_raw(k);
        pks(end+1)=pks_raw(k);
    elseif pks_raw(k)>pks(end)
        locs(end)=locs_raw(k);
        pks(end)=pks_raw(k);
    end
end

```
Se emplea *findpeaks* para localizar los picos respiratorios. Luego se filtran picos falsos con un tiempo mínimo entre respiraciones, asegurando una detección confiable.

### 6. Calculo de Frecuencia Respiratoria
```
Nresp = numel(locs);

if Nresp > 1
    T_eff = locs(end)-locs(1);
    FR_media = 60*(Nresp-1)/T_eff;
else
    FR_media = 0;
end

T_resp = diff(locs);
SDRR  = std(T_resp);
RMSSD = sqrt(mean(diff(T_resp).^2));
CV = SDRR/mean(T_resp);

fprintf("\n====== CARACTERÍSTICAS RESPIRATORIAS ======\n");
fprintf("Respiraciones detectadas: %d\n",Nresp);
fprintf("Frecuencia respiratoria media: %.2f rpm\n",FR_media);
```
A partir de los picos detectados se calcula la frecuencia respiratoria media en rpm y métricas de variabilidad como SDRR, RMSSD y coeficiente de variación.

### 7. Filtrado de la Señal 
```
resp_amp = detrend(v_f);
resp_amp = resp_amp/max(abs(resp_amp));
resp_amp = 1.5*resp_amp;
fc = 0.6;
[b,a] = butter(4, fc/(Fs/2), 'low');
resp_filt = filtfilt(b,a,resp_amp);

```
Se normaliza y se aplica un filtro Butterworth pasa bajas para eliminar ruido de alta frecuencia y resaltar la señal respiratoria.

### 8. Analisis En Frecuencia 
```
N = length(resp_filt);
Y = fft(resp_filt);
f = (0:N-1)*(Fs/N);
P = abs(Y/N);

idx = f<=1;
f_dom = f(idx);
P_dom = P(idx);

[~,imax] = max(P_dom);
f_peak = f_dom(imax);
FR_dom = f_peak*60;

fprintf("Frecuencia dominante (FFT): %.2f rpm\n",FR_dom);

```
Se calcula la Transformada Rápida de Fourier de la señal filtrada para identificar la frecuencia dominante asociada a la respiración.

### 9. Guardado Automático 
```
files = dir('Muestra_*.mat');

if isempty(files)
    nextNum = 1;
else
    nums = zeros(length(files),1);
    for i=1:length(files)
        name = files(i).name;
        num = sscanf(name,'Muestra_%d.mat');
        nums(i) = num;
    end
    nextNum = max(nums)+1;
end

filename = sprintf('Muestra_%d.mat',nextNum);

save(filename,'t','v','v_f','resp_filt','locs','pks','FR_media','FR_dom');

fprintf("\nArchivo guardado como: %s\n",filename);
```
El sistema guarda cada adquisición en archivos secuenciales (Muestra_1.mat, Muestra_2.mat, etc.), almacenando tanto la señal como los parámetros calculados.

### 10. Visualización Final 
```
figure("Name","Reconstrucción Respiratoria","Color","w");

subplot(2,1,1)
plot(t,v_f,'k','LineWidth',1.2); hold on;
plot(locs,pks,'ro'); grid on;
title("Señal respiratoria con picos");

subplot(2,1,2)
plot(f_dom,P_dom,'b','LineWidth',1.2); hold on;
plot(f_peak,P_dom(imax),'ro','MarkerSize',8,'LineWidth',2);
grid on;
xlabel("Frecuencia (Hz)");
title(sprintf("FFT (%.2f rpm)",FR_dom));

end
```
Se muestran dos gráficas: 
- La señal respiratoria con picos detectados.
- El espectro de frecuencia con el pico dominante resaltado.

## Resultados y Análisis de Resultados 
### 1. Respiración en Reposo 
La señal adquirida en tiempo real cuando el sujeto de prueba se encuentra es reposo es:
![WhatsApp Image 2026-02-11 at 9 02 04 PM](https://github.com/user-attachments/assets/800aaaec-de54-44a5-bb34-de5f0ef16455)
Despues de la adquision en tiempo real se obtienen resultados de la señal original filtrada y en sus componentes en frecuencia.
![WhatsApp Image 2026-02-11 at 9 02 43 PM](https://github.com/user-attachments/assets/3ee965e6-0603-4c63-b4b7-6151b6f33b99)
La señal respiratoria en el dominio del tiempo muestra un comportamiento periódico y estable, característico de una respiración en reposo. Los ciclos presentan amplitud y forma relativamente constantes, lo que indica un patrón respiratorio regular sin episodios de apnea, hiperventilación o irregularidades marcadas al filtrar la señal  se puede observar con mayor claridad las oscilaciones respiratorias al reducir el ruido de alta frecuencia, facilitando la detección de los picos asociados a cada ciclo de inhalación–exhalación. Los picos identificados se encuentran espaciados de manera uniforme, lo que respalda una respiración rítmica y fisiológicamente normal.

En el dominio de la frecuencia, el espectro obtenido mediante la FFT presenta una frecuencia dominante cercana a 0.27 Hz, equivalente aproximadamente a 16 respiraciones por minuto, valor que se encuentra dentro del rango normal para un adulto en reposo (12–20 rpm). La concentración de energía alrededor de esta frecuencia indica que la señal está dominada por un único componente respiratorio principal, con mínima contribución de componentes armónicas o ruido. En el comand window se muestran las caracteristicas respiratorias obtenidas de la señal al usuario.
<p align="center">
  <img src="https://github.com/user-attachments/assets/31f787ad-4f7b-45c4-bbc9-8658c63fa68c" width="350">
</p>
Esto confirma la coherencia entre el análisis temporal y frecuencial, y valida el procesamiento aplicado, demostrando que el sistema es capaz de caracterizar adecuadamente la dinámica respiratoria en condiciones de reposo.

### 2. Respiracion Hablando o Leyendo 
La señal adquirida en tiempo real cuando el sujeto de prueba se encuentra es leyendo es:
![WhatsApp Image 2026-02-11 at 9 10 26 PM](https://github.com/user-attachments/assets/b1ae4a0d-6422-4793-9510-777a30a948ab)
Despues de la adquision en tiempo real se obtienen resultados de la señal original filtrada y en sus componentes en frecuencia.
![WhatsApp Image 2026-02-11 at 9 10 52 PM](https://github.com/user-attachments/assets/7e2deabd-31be-4d41-8eac-87de3435f43f)
En el dominio del tiempo, la señal respiratoria presenta mayor variabilidad en amplitud y forma en comparación con el estado de reposo. Las oscilaciones son menos regulares y muestran pequeñas deformaciones en los ciclos, lo cual es consistente con el acto de hablar, ya que la respiración se ve interrumpida por la fonación y por patrones respiratorios irregulares. Aun así, los picos detectados mantienen una periodicidad global, permitiendo identificar los ciclos respiratorios principales, aunque con ligeras variaciones en su duración. Este comportamiento refleja un control respiratorio más activo y no automático, típico de una respiración asociada al habla.

En el dominio de la frecuencia, la FFT muestra una frecuencia dominante cercana a 0.23 Hz, correspondiente aproximadamente a 14 respiraciones por minuto, valor aún dentro del rango fisiológico normal. Sin embargo, el espectro presenta una mayor dispersión de energía en frecuencias bajas adicionales, lo que indica la presencia de componentes secundarias asociadas a pausas, frases cortas y cambios en el ritmo respiratorio durante el habla. Esta distribución más ancha confirma que la señal no es estrictamente periódica, pero el pico principal sigue representando adecuadamente la frecuencia respiratoria media del sujeto en esta condición.

En el comand window se muestran las caracteristicas respiratorias obtenidas de la señal al usuario.
<p align="center">
  <img src="https://github.com/user-attachments/assets/60255747-4880-425a-a1ea-8218f2ebe788" width="350">
</p>

Los resultados indican una frecuencia respiratoria media de 13.51 rpm, coherente con una respiración controlada durante el habla. La frecuencia dominante obtenida mediante FFT (14.00 rpm) confirma la consistencia del análisis en los dominios temporal y frecuencial.

Al realizar una comparativa entre los dos modos en los que se midio la frecuencia respiratoria se encuntra que en reposo, el patrón respiratorio del individuo presenta mayor regularidad y simétria, con ciclos casi periódicos y una relación equilibrada entre inhalación y exhalación; la frecuencia se mantiene estable dentro del rango fisiológico normal. Durante la verbalización, la respiración se vuelve más irregular, ya que la exhalación se prolonga para permitir el habla y las inhalaciones se acortan, lo que modifica la relación entre ambas fases y genera mayor variabilidad en la señal, aunque la frecuencia media continúa dentro de valores normales.
El sistema desarrollado demuestra un alto potencial como herramienta de monitoreo respiratorio básico, ya que permite identificar variaciones en la frecuencia, regularidad y estabilidad del patrón respiratorio. Estas métricas pueden ser útiles como indicadores preliminares de alteraciones fisiológicas, como taquipnea, bradipnea o irregularidades respiratorias, lo que lo convierte en un recurso valioso para prácticas educativas, monitoreo no invasivo y seguimiento en entornos controlados.

El alcance la solucion implementada demuestra un alto potencial como herramienta de monitoreo respiratorio básico, ya que permite identificar variaciones en la frecuencia, regularidad y estabilidad del patrón respiratorio. Estas métricas pueden ser útiles como indicadores preliminares de alteraciones fisiológicas, como taquipnea, bradipnea o irregularidades respiratorias, lo que lo convierte en un recurso valioso para prácticas educativas, monitoreo no invasivo y seguimiento en entornos controlados. No obstante, su capacidad para detectar patologías es limitada, debido a que el sensor MQ-3 no es específico para CO₂ y responde a múltiples gases, lo que puede introducir errores. Además, factores como la posición del sensor, la humedad, el ruido ambiental y la falta de calibración clínica afectan la precisión.

## Conclusiones 

- Se comprobó que la verbalización influye directamente en el patrón respiratorio, generando ciclos más irregulares y una modificación en la relación entre inhalación y exhalación, en comparación con la respiración en reposo, donde el comportamiento es más estable y periódico.

- Se lograron identificar las principales variables físicas involucradas en el proceso respiratorio, como la variación de la señal en el tiempo, la frecuencia respiratoria y la amplitud, las cuales permiten caracterizar adecuadamente el comportamiento del sistema respiratorio.

- El sistema desarrollado fue capaz de extraer el patrón respiratorio a partir de la señal adquirida y estimar de forma confiable la frecuencia respiratoria, tanto en el dominio del tiempo como en el dominio de la frecuencia mediante transformada rápida de Fourier (FFT), demostrando un alto potencial como herramienta de monitoreo respiratorio básico y como base para el desarrollo de aplicaciones biomédicas más avanzadas.

## Bibliografía 

- Nicolò, A., Massaroni, C., Schena, E., Sacchetti, M. *The Importance of Respiratory Rate Monitoring: From Healthcare to Sport and Exercise*. Sensors, 2020.  
- Charlton, P. H., Birrenkott, D. A., Bonnici, T., Pimentel, M. A. F., Johnson, A. E. W., Alastruey, J., Tarassenko, L., Watkinson, P. J., Beale, R., Clifton, D. A. *Breathing Rate Estimation From the Electrocardiogram and Photoplethysmogram: A Review*. IEEE Reviews in Biomedical Engineering, 2018.
- Gazitúa, R. *Respiración*. (incluido en definiciones de frecuencia respiratoria en fuentes enciclopédicas).
- Rodríguez-Molinero, A., et al. *Normal respiratory rate and peripheral blood oxygen saturation in the elderly population*. Journal of the American Geriatrics Society, 2013.
- McArdle, W. D., Katch, F. I., Katch, V. L. *Exercise Physiology: Energy, Nutrition, and Human Performance*. Lippincott Williams & Wilkins, 2006.
- González, J., Arenas, O., González V. *Valores de la frecuencia respiratoria*. Universidad Nacional Autónoma de Nicaragua (2012).
- LibreTexts Español. *Fundamentos Respiratorios: Frecuencia Respiratoria y Control de Ventilación* (educational text).

</div>

