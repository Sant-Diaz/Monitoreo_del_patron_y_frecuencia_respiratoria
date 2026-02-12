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
Se muestran dos gráficas: la señal respiratoria con picos detectados y el espectro de frecuencia con el pico dominante resaltado.

## Resultados y Análisis de Resultados 
