# Nano ORYKSA

[![English](https://img.shields.io/badge/English-30363d?style=for-the-badge)](README.md) [![Português](https://img.shields.io/badge/Portugu%C3%AAs-30363d?style=for-the-badge)](README.pt.md) [![Español](https://img.shields.io/badge/Espa%C3%B1ol-0891b2?style=for-the-badge)](README.es.md) [![Français](https://img.shields.io/badge/Fran%C3%A7ais-30363d?style=for-the-badge)](README.fr.md)

**La IA sin conexión de la app móvil de ORYKSA.**

Cuando el teléfono pierde la señal - en un avión, en un túnel, en un sótano - el asistente
de ORYKSA no se queda a oscuras. Una versión más pequeña de ella, **Nano ORYKSA**, toma el
relevo desde dentro del teléfono. Es más limitada que la ORYKSA con la que hablas en línea,
pero lleva la memoria consigo: tu perfil, tus servicios, tus precios, tu horario de
apertura y todo tu Brain.

Este repositorio aloja los archivos del modelo que la app descarga. Nada de lo que hay aquí
se ejecuta en un servidor: todo está pensado para ejecutarse en el propio teléfono.

Desarrollado por **Weslley Harakawa** - [ORYKSA](https://oryksa.com)

---

## Qué hace Nano ORYKSA sin conexión

- Responde sobre tu negocio, a partir de la memoria sincronizada con el teléfono
- Anota todo lo que le pidas cambiar y lo ejecuta en cuanto vuelvas a tener conexión
- Conversa contigo y te ayuda a calmarte cuando estás estresado o ansioso
- Da números de emergencia y primeros auxilios básicos, sin ninguna conexión

## Qué no puede hacer sin conexión

- Leer mensajes nuevos de clientes (esos viven en el servidor)
- Reservar citas ni cambiar tu cuenta (pasan a una cola)
- Buscar en la web

Lo dice con claridad en lugar de fingir. Todo lo que necesita el servidor se pone en cola
y se ejecuta, uno por uno, en cuanto el teléfono vuelve a tener conexión.

---

## Cómo elige la app un cerebro

| Teléfono | Qué se ejecuta | Descarga |
|---|---|---|
| iPhone 15 Pro y posteriores, iOS 26 con Apple Intelligence | el modelo que Apple ya incluye en iOS | **ninguna** |
| iPhones más antiguos y Android | el modelo publicado en este repositorio | opcional, bajo demanda |
| Cualquier otro | búsqueda en la memoria, sin ningún modelo | ninguna |

La app de ORYKSA en las tiendas **nunca incluye un modelo**. Se mantiene pequeña. La IA sin conexión
solo se descarga si el dueño la pide, y se puede eliminar en cualquier momento para liberar
espacio.

## La memoria

Antes de que se pierda la señal, la app guarda una copia de todo lo que Nano ORYKSA necesita
saber. Es texto, medido en kilobytes, obtenido de `GET /api/app/offline-pack`
y actualizado automáticamente cada vez que la app se abre o vuelve a la pantalla.

## Versiones

Los archivos del modelo se publican como archivos de versión (release assets). La app lee la dirección de descarga
del backend de ORYKSA, así que el modelo se puede cambiar o desactivar sin
publicar una nueva versión de la app.

| Archivo | Modelo | Tamaño | Formato |
|---|---|---|---|
| `oryksa-nano.gguf` | Gemma 3 1B Instruct (Q4_K_M) | 778 MB | GGUF |

## Licencia de los modelos

Los pesos de los modelos publicados aquí mantienen la licencia de sus autores originales.
Gemma se distribuye bajo los [Gemma Terms of Use](https://ai.google.dev/gemma/terms)
de Google. Usar este repositorio implica aceptar esos términos.

## Sobre el autor

**Weslley Harakawa** - Fundador de ORYKSA AI y Chief Innovation Officer de Harakawa Tech. En Lisboa, Portugal. Especialidades: inteligencia artificial, desarrollo web y móvil, tokenización en blockchain. Formación: University of the People.

- Sitio web: https://harakawa.tech
- LinkedIn: https://www.linkedin.com/in/weslleyharakawa/
- Instagram: https://www.instagram.com/weslley.harakawa
- ORYKSA AI Employees: https://oryksa.com (X: https://x.com/oryksa, Instagram: https://www.instagram.com/oryksaai, YouTube: https://www.youtube.com/@ORYKSA)

El nombre, la marca y la app ORYKSA son propiedad de Weslley Harakawa.
