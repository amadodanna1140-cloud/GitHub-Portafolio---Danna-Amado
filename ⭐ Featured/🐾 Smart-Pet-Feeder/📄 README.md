# 🐾 Smart Pet Feeder

<p align="center">
  <img width="200" alt="Smart Pet Feeder - Prototipo final" src="https://github.com/user-attachments/assets/879790db-81cd-46e1-a618-0ad2ec88f9ff" />
  <img width="200" alt="Smart Pet Feeder - Prototipo final" src="https://github.com/user-attachments/assets/2eb52929-e004-4654-aae5-2f3fcacd3e7f"/>
</p>
<p align="center">
  <em>Vista exterior y distribución interna del Smart Pet Feeder.</em>
</p>

> Sistema automatizado para la dispensación programada de alimento para mascotas, desarrollado con Arduino e integración de componentes electrónicos y una estructura fabricada mediante impresión 3D.

## 📌 Sobre el proyecto

Smart Pet Feeder es un dispensador automático de alimento para mascotas diseñado para automatizar la alimentación mediante la configuración de porciones e intervalos de tiempo.

El sistema integra un microcontrolador Arduino, un reloj de tiempo real, un servomotor de rotación continua, una pantalla OLED y botones de interacción para permitir al usuario configurar y controlar el proceso de alimentación.

El prototipo fue desarrollado, ensamblado, programado y probado hasta alcanzar un funcionamiento completamente operativo. Este proyecto hizo parte del trabajo realizado durante mi formación académica y contribuyó a mi graduación con honores.

## 🎯 Objetivo

Desarrollar un sistema capaz de automatizar la alimentación de una mascota, permitiendo al usuario establecer:

* La cantidad de porciones a dispensar.
* El intervalo de tiempo entre cada porción.
* La activación manual del mecanismo de dispensación.

El objetivo principal fue crear una solución funcional que redujera la necesidad de realizar manualmente cada alimentación y que pudiera evolucionar posteriormente hacia un sistema conectado.

## ⚙️ ¿Cómo funciona?

El sistema utiliza un **RTC DS3231** para mantener y consultar la hora actual. El usuario configura el número de porciones y el intervalo de alimentación mediante los botones físicos del dispositivo.

Una vez configurado, Arduino utiliza la información del RTC para determinar cuándo debe realizarse la siguiente dispensación y activa el servomotor encargado de liberar el alimento.

La pantalla OLED permite visualizar en todo momento:

* Cantidad de porciones configuradas.
* Intervalo establecido entre las porciones.
* Hora actual.

Además, el sistema incorpora un botón de activación manual que permite dispensar alimento sin esperar al siguiente intervalo programado.

### Flujo general

```text
Usuario
   │
   ├── Configura porciones
   ├── Configura intervalo
   └── Activación manual
           │
           ▼
       Arduino Nano
           │
     ┌─────┴─────┐
     │           │
     ▼           ▼
 RTC DS3231    OLED
     │
     ▼
 Control de tiempo
     │
     ▼
 Servomotor
     │
     ▼
 Dispensación de alimento
```

## 🛠️ Tecnologías utilizadas

### Hardware

* Arduino Nano
* Arduino Uno — utilizado durante las pruebas y demostración de funcionamiento
* RTC DS3231
* Servomotor MG995 de rotación continua
* Pantalla OLED
* 3 botones de control
* Buzzer
* PCB de prototipado
* Convertidor reductor a 5 V
* Conector Jack de alimentación

### Software

* Arduino IDE
* Programación en C/C++ para Arduino

### Fabricación

* Diseño de carcasa mediante impresión 3D
* PLA
* Boquilla de 0,4 mm
* Altura de capa de 0,25 mm
* 20 % de relleno
* 2 perímetros
* Impresión sin soportes

## ✨ Características principales

* 🍽️ Dispensación automática de alimento.
* 🔢 Configuración de **1 a 15 porciones**.
* ⏱️ Configuración del intervalo entre porciones.
* 🕐 Reloj en tiempo real mediante RTC DS3231.
* 🖥️ Visualización de información mediante pantalla OLED.
* 🔘 Control mediante botones físicos.
* ▶️ Activación manual del servomotor.
* 🔊 Buzzer para interacción/notificaciones.
* ⚙️ Servomotor modificado para permitir rotación continua.
* 🖨️ Estructura física fabricada mediante impresión 3D.
* ✅ Prototipo completamente funcional.

## 🏗️ Arquitectura y escalabilidad

El proyecto fue planteado teniendo en cuenta la posibilidad de ampliar sus funcionalidades posteriormente.

La versión desarrollada funciona como un sistema autónomo, donde Arduino concentra la lógica de control, recibe las configuraciones del usuario, consulta el RTC y controla el mecanismo de dispensación.

Durante el desarrollo se realizaron pruebas con diferentes placas. Inicialmente se presentaron inconvenientes con una placa Arduino Nano, por lo que se utilizó un Arduino Uno para demostrar y validar el funcionamiento del sistema. Posteriormente, se incorporó otra placa Arduino Nano en la versión final.

Esta experiencia permitió validar el funcionamiento del sistema y resolver problemas relacionados con la integración entre hardware y software.

## 📱 Proyección futura

Como evolución del proyecto, se planteó la implementación de una aplicación móvil que permitiera interactuar remotamente con el dispensador.

La aplicación propuesta tendría como funciones:

* Configurar la cantidad de porciones.
* Configurar los intervalos de alimentación.
* Activar manualmente el servomotor.
* Dispensar alimento bajo demanda.

La aplicación móvil **no llegó a desarrollarse ni cuenta con una implementación funcional dentro de este proyecto**; corresponde a una propuesta de expansión futura.

También se planteó una segunda etapa de evolución mediante la incorporación de:

* 📷 Cámara para supervisar a la mascota.
* 🔊 Bocina o micrófono para añadir funcionalidades de comunicación y monitoreo desde la aplicación.


## 🧠 Aprendizajes

Este proyecto permitió desarrollar experiencia práctica en:

* Programación de microcontroladores.
* Integración de componentes electrónicos.
* Manejo de módulos RTC.
* Control de servomotores.
* Interfaces físicas mediante botones y pantalla OLED.
* Depuración y resolución de problemas de hardware y software.
* Modificación de componentes para adaptar su funcionamiento.
* Fabricación de prototipos mediante impresión 3D.
* Integración entre software y hardware.
* Diseño de soluciones pensando en futuras posibilidades de escalabilidad.

Uno de los principales aprendizajes fue el proceso de **prueba, identificación de problemas y adaptación de la solución**, especialmente durante las dificultades encontradas con las placas Arduino y la pantalla OLED.

## 📸 Galería

A continuación se muestran algunos elementos del proceso de diseño, construcción, programación y ensamblaje del **Smart Pet Feeder**.

### 🧩 Diseño y esquema

**Esquema del sistema**

<img width="250" alt="Esquema del sistema" src="https://github.com/user-attachments/assets/cd8369ee-6005-471d-a531-c5f9346c5a47" />

---

### 🔌 Integración electrónica

**Unión y conexión de componentes**

<img width="250" alt="Unión de componentes" src="https://github.com/user-attachments/assets/cc0c5e4b-a7b4-4318-87ba-e1a7bfefecfd" />

---

### 💻 Desarrollo y depuración

Durante el desarrollo se realizaron diferentes pruebas de programación y procesos de depuración para solucionar los inconvenientes encontrados durante la integración del sistema.

**Errores encontrados durante la programación**

<img width="250" alt="Errores de programación" src="https://github.com/user-attachments/assets/84c932b5-7afa-4069-b3ff-caf46472624d" />

---

### 🏗️ Construcción

**Construcción inicial del prototipo**

<img width="500" alt="Construcción inicial" src="https://github.com/user-attachments/assets/169d744f-3d33-4a4e-a0b3-3c27c5cbaac5" />

---

### 🖨️ Diseño e impresión 3D

**Archivos STL utilizados para la fabricación de la estructura**

<img width="500" alt="Archivos STL" src="https://github.com/user-attachments/assets/4949303a-4e06-4e2f-8648-79cdbc450688" />

**Prototipo físico**

<img width="500" alt="Prototipo físico" src="https://github.com/user-attachments/assets/f61c2f28-04c3-4774-b276-6aa06e4b09fa" />

---

### 🔬 Prototipo funcional — Arduino UNO

Antes de integrar la versión final con Arduino Nano, se utilizó un **Arduino UNO como plataforma de prueba y validación**.

Esta etapa permitió comprobar el funcionamiento del sistema, verificar la comunicación entre los diferentes componentes y realizar las pruebas necesarias antes de implementar la versión final del prototipo.

<p align="center">
<img width="200" alt="Prototipo funcional con Arduino UNO" src="https://github.com/user-attachments/assets/e9c1ffae-84ce-48de-8f8f-f8c3e1f1c354"/>
</p>
<p align="center">
  <em>Montaje del prototipo durante la etapa de pruebas y validación.</em>
</p>

### 🐾 Resultado del desarrollo

Estas imágenes documentan parte del proceso mediante el cual el diseño conceptual se convirtió en un prototipo físico funcional.




