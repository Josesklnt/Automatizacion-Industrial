## 🏭 Modernización y Automatización: Planta de Harina Precocida (7 Niveles)

> **Proyecto:** Reingeniería integral del sistema de control y supervisión tras años de inactividad técnica y obsolescencia de hardware.

### 🌐 Arquitectura de Red y Comunicaciones (Topología OT)

El diseño se basó en una infraestructura híbrida para garantizar determinismo en campo y velocidad en supervisión:

* **Backbone Ethernet (Estrella):** Interconexión de **4 DCS Ascon SigmaPAC** con el sistema **SCADA** central y **7 HMI Touchscreen**.
* **Distribución HMI:** 4 estaciones cada una conectadas directamente a los DCS y 3 vía Switch industrial, permitiendo la operación local en cada uno de los 7 pisos de la planta.


* **Bus de Campo CanOpen:** Utilizado para la expansión de E/S. Los DCS actuaban como maestros, comunicándose con los módulos de entradas/salidas digitales y analógicas mediante este **robusto protocolo**.

### 📊 Capa de Visualización y Control (SCADA/HMI)

Se implementó una solución de supervisión centralizada para la gestión operativa y de activos:

* **Software:** **Indusoft Web Studio v8** (actualmente AVEVA Edge).
* **Instrumentación y Variables Críticas:**
* **Almacenamiento:** Niveles de silos mediante transmisores por ultrasonido.
* **Molienda:** Nivel, temperatura en **molinos tipo martillo**, sensores de proximidad en puertas, ajuste de masas, presión y velocidad.
* **Transporte y Dosificación:** Presión de aire en transporte neumático, celdas de carga (galgas) en balanzas por golpeteo con integración de caudal, velocidad en cangilones (lado libre) y **sensores en puertas de sinfines**.
* **Proceso Térmico:** **Control de temperatura en secador y cocina**, control de caudal de agua en humidificadores y válvulas de compuertas.


* **Funcionalidades Avanzadas:** Sinópticos de proceso, estaciones de control, gestión de alarmas, tendencias (Trending), históricos, estatus de salud de los DCS, diagramas unifilares y parámetros eléctricos.

### 🛠️ Historia Técnica (Business Case)

#### **El Reto Operativo**

Tras un accidente y años de paralización, la humedad crítica inutilizó la electrónica existente (Tarjetas de control y PLC). La planta carecía de operatividad y el hardware original era irrecuperable.

#### **La Solución Implementada**

Se sustituyó la tecnología obsoleta por una arquitectura **DCS Ascon** programada bajo el estándar **IEC 61131-3 (OpenPCS)**. La ubicación estratégica de las Touchscreens eliminó la necesidad de desplazamiento vertical constante entre los 7 niveles, centralizando la toma de decisiones en una sala de control principal.

#### **Impacto y Resultados**

* **Restauración Total:** Recuperación de la operatividad al 100% de la planta.
* **Eficiencia Estimada:** Mejora del **30%** en la eficiencia de procesos, permitiendo la reinversión del ahorro en fases subsiguientes de automatización.
* **Seguridad:** Implementación de interlocks de seguridad y secuencias automáticas de motores (Interlock de motores) para prevenir fallas operativas.

---

### 🛠️ Tecnologías Clave

* **Control:** DCS Ascon SigmaPAC.
* **HMI:** Ascon Touchscreen (7 unidades).
* **SCADA:** Indusoft Web Studio v8 (AVEVA).
* **Protocolos:** Ethernet TCP/IP, CanOpen.
* **Estándar de Programación:** IEC 61131-3.
