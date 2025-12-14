# Gestor-de-inversiones

Este proyecto es un sistema integral para gestionar inversiones en bolsa y criptoactivos de forma automatizada. Utiliza **n8n** como orquestador, **Google Sheets** como base de datos y **Agentes de IA** para interpretar comandos y resumir noticias financieras.

El sistema se divide en **3 flujos de trabajo (workflows)** principales que operan en conjunto:

---

## 🚀 Módulos del Sistema

### 1. Bot de Trading (Telegram + AI Agent)

Es la interfaz principal del usuario. A través de un bot de Telegram, puedes interactuar con tu cuenta de inversiones usando lenguaje natural.

- **Gestión de Usuarios:** Registro automático y creación de cuentas.
    
- **Operaciones:** Compra y venta de activos (Acciones/Cripto) mediante órdenes de tipo **MARKET** (inmediata) o **LIMIT** (precio objetivo).
    
- **Consultas Inteligentes:** Gracias a un agente de LangChain, puedes preguntar:
    
    - _"¿Cuál es el precio de Apple?"_
        
    - _"Muéstrame mi portafolio"_
        
    - _"Agrega Tesla a mis favoritos"_
        
- **Persistencia:** Todo se guarda en tiempo real en Google Sheets (Usuarios, Transacciones, Portfolio).
    

### 2. Daily Market News (Email Digest)

Un asistente informativo que te mantiene al día sin saturarte.

- **Resumen Diario:** De lunes a viernes (09:15 AM), el sistema revisa tu lista de acciones "Favoritas".
    
- **Búsqueda y Filtrado:** Consulta las últimas noticias relevantes en **Finnhub**.
    
- **Análisis con IA:** Un modelo GPT lee las noticias y redacta un **resumen ejecutivo en español**.
    
- **Entrega:** Recibes un correo electrónico formateado en HTML con el resumen y los enlaces originales.
    

### 3. Ejecutor de Órdenes (Trading Engine)

El motor silencioso que corre en segundo plano (cada minuto).

- **Monitoreo de Precios:** Verifica constantemente el precio de mercado de los activos en órdenes pendientes usando **Alpha Vantage**.
    
- **Ejecución Automática:**
    
    - Si una orden **LIMIT** alcanza su precio objetivo (Buy o Sell), se ejecuta automáticamente.
        
    - Procesa las órdenes **MARKET** de inmediato.
        
- **Actualización de Saldos:** Al ejecutarse una orden, el sistema actualiza automáticamente tu saldo disponible en la cuenta y la cantidad de activos en tu portafolio.
    

---

## 🛠️ Stack Tecnológico

- **Orquestación:** [n8n](https://n8n.io/)
    
- **Base de Datos:** Google Sheets
    
- **Inteligencia Artificial:** OpenAI (GPT-4o / GPT-4o-mini)
    
- **Interfaz:** Telegram Bot API
    
- **Datos Financieros:** Alpha Vantage & Finnhub
    
- **Notificaciones:** Gmail & Telegram
    

---

## 📋 Requisitos Previos

Para desplegar este proyecto necesitas:

1. Una instancia de **n8n** (Self-hosted o Cloud).
    
2. Cuentas y API Keys de: **OpenAI**, **Telegram**, **Alpha Vantage** y **Finnhub**.
    
3. Credenciales de Google Cloud habilitadas para **Google Sheets** y **Gmail**.
    
4. La estructura de Google Sheets proporcionada (Usuarios, Favoritos, Portfolio, Transacciones, Órdenes).
    

---

**Disclaimer:** Este software es un proyecto educativo y experimental. No constituye una recomendación de inversión financiera.
