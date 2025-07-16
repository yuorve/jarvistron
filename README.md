Jarvistron Bot: Domótica y Alertas Inteligentes con Alexa, Telegram y Automatización
Me complace compartir mi proyecto personal: Jarvistron Bot, una solución de domótica inteligente que integra Amazon Alexa, Telegram, n8n y Google Sheets para mejorar la seguridad y el monitoreo del hogar. Este prototipo, nacido de mi interés en la automatización, demuestra cómo se pueden interconectar diversas plataformas para crear un sistema de alertas proactivo y un registro de actividad.

¿Cómo funciona Jarvistron Bot?
El corazón de Jarvistron Bot reside en la orquestación de sus componentes:

Amazon Alexa (Jarvistron Bot Skill): Es el punto de entrada principal. A través de rutinas de Alexa activadas por los sensores de mi casa (Xiaomi Home, eWelink, Tuya, integrados en Home Assistant), la skill envía información relevante a mi sistema.

n8n (Automatización y Conexión): Este orquestador clave maneja dos flujos de trabajo principales:

Webhook para Google Sheets: Recibe los datos de la skill de Alexa, activado por un webhook, y los registra automáticamente en una hoja de Google Sheets.

Gestión del Bot de Telegram: Actúa como disparador cuando el bot de Telegram recibe mensajes. Permite enviar mensajes de alerta y consultar los registros de Google Sheets a través del bot.

Telegram Bot (Alertas en Tiempo Real): Recibe avisos instantáneos sobre eventos importantes, como "puertas abiertas" o "sensores de movimiento activados", directamente en mi dispositivo móvil a través de la API de Telegram.

Google Sheets (Registro y Análisis): Almacena un historial detallado de los eventos de los sensores. Estos registros son cruciales para el seguimiento de la actividad y la seguridad, proporcionando una visión clara de lo que ocurre en casa.

Arquitectura de Despliegue y Conectividad Segura
Un aspecto clave de este proyecto es su robusta arquitectura de despliegue:

Tanto Home Assistant como n8n están configurados como contenedores Docker dentro de mi red local.

La exposición segura de estos servicios a internet se realiza mediante Cloudflare Tunnels. Esto permite que la Amazon Skill (que necesita acceder al webhook de n8n) y otras integraciones externas se comuniquen con mi red interna de forma segura, sin necesidad de abrir puertos en el router, lo que refuerza la seguridad y la privacidad.

Beneficios y Futuro del Proyecto
Aunque el principal motor de este proyecto ha sido la curiosidad y el aprendizaje en el ámbito de la automatización y la interconexión de sistemas, Jarvistron Bot ofrece beneficios tangibles como:

Monitoreo Proactivo: Recibe alertas cruciales sobre la actividad en casa, aumentando la seguridad.

Registro Histórico: Mantiene un registro detallado de eventos para análisis y seguimiento.

Integración Versátil: Demuestra la capacidad de integrar diversas tecnologías (voz, domótica, automatización low-code, bases de datos) en una solución cohesiva.

Despliegue Robusto y Seguro: Utiliza tecnologías modernas como Docker y Cloudflare Tunnels para una infraestructura fiable y protegida.

Este prototipo es una base sólida, y ya estoy explorando cómo expandir sus capacidades, como permitir el control de la domótica directamente desde el bot de Telegram.

¿Por qué es relevante para ti?
Este proyecto showcase mis habilidades en:

Desarrollo de Amazon Alexa Skills

Automatización con n8n (integraciones, webhooks, flujos de trabajo)

Gestión de APIs (Telegram API)

Integración de Sistemas Domóticos (Home Assistant, Xiaomi Home, eWelink, Tuya)

Manejo de Datos (Google Sheets para registro y consulta)

Contenerización con Docker

Configuración de Redes y Seguridad (Cloudflare Tunnels)

Resolución de Problemas y Pensamiento Lógico

Si buscas un perfil con experiencia práctica en la creación de soluciones innovadoras y automatizadas, o si te interesa discutir posibles aplicaciones de esta tecnología, no dudes en contactarme.
