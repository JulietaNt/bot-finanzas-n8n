# bot-finanzas-n8n
# 🤖 Bot de Finanzas Personales con IA + n8n

Automatización para registrar, organizar y consultar gastos e ingresos usando lenguaje natural.

---

## 🎯 Problema

Muchas personas y pequeños negocios no llevan un control claro de sus finanzas.

- registrar gastos manualmente es incómodo
- se pierde información o se anota mal
- no hay una visión clara de en qué se va el dinero
- las herramientas existentes suelen ser poco prácticas o demasiado complejas

---

## 💡 Solución

Desarrollé un bot de Telegram que permite registrar y consultar movimientos financieros simplemente escribiendo mensajes, como si estuvieras hablando.

Por ejemplo:
- “gasté 6000 en transporte”
- “cobré 1000 dólares del trabajo”
- “¿cuánto gasté hoy?”

El sistema interpreta el mensaje, procesa los datos automáticamente y los guarda en Google Sheets.

---

## ⚙️ Cómo funciona

1. El usuario envía un mensaje por Telegram  
2. Un AI Agent interpreta la intención (registro / consulta / chat)  
3. Un nodo en JavaScript procesa y estructura los datos  
4. Se decide el flujo con un Switch (registrar / consultar)  
5. Los datos se guardan o se consultan desde Google Sheets  
6. El bot responde automáticamente al usuario  

---

## 🧠 Decisiones técnicas

- Separación entre interpretación (IA) y lógica de negocio (JavaScript)
- Uso de detección de acciones (`REGISTRAR`, `CONSULTA`) para controlar el flujo
- Parsing de JSON desde la respuesta del modelo
- Manejo de errores en la interpretación de datos
- Integración con API externa para obtener tipo de cambio en tiempo real
- Soporte para múltiples monedas (ARS / USD) con conversión automática
- Normalización de datos antes de guardarlos

---

## 📸 Ejemplo de funcionamiento

### 🔁 Flujo en n8n
![Flujo](Screenshots/flujo.png)

### 💬 Interacción con el bot (Telegram)
![Telegram](Screenshots/telegram.png)

### 📊 Datos almacenados en Google Sheets
![Sheets](Screenshots/sheets.png)

### 🧠 Lógica de procesamiento (código)
![Código](Screenshots/codigo.png)

---

## 🚀 Aplicaciones

Este tipo de automatización puede adaptarse fácilmente para:

- control de finanzas personales
- registro de ventas en negocios
- seguimiento de ingresos y egresos
- automatización de reportes simples
- asistentes internos para pequeñas empresas

---

## 🔧 Tecnologías utilizadas

- n8n
- OpenAI / AI Agent
- Telegram Bot API
- Google Sheets
- JavaScript

---

## 📦 Cómo usarlo

1. Importar el archivo JSON en n8n  
2. Configurar credenciales:
   - Telegram Bot  
   - OpenAI API  
   - Google Sheets  
3. Ejecutar el workflow  

---

## 📌 Nota

Este proyecto fue desarrollado como práctica de automatización, pero pensado con un enfoque aplicado a casos reales, como control financiero y automatización de procesos.
