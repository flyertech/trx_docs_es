---
title: Webhook / trackear los leads
sidebar: mydoc_sidebar
permalink: webhook.html
folder: mydoc
---

## Vista general
**Transactionale** Transactionale se encarga de todo el proceso de generación de leads por ti. Pero si tienes los recursos necesarios, es una genial idea si aprovechas las ventajas de Transactionale **webhook** para mejorar el rendimiento.

Hemos creado esta característica para ayudarte a **importar los leads automáticamente en tu plataforma** y así puedes implementar tus propias estrategias de marketing con ellos.
Con el webhook, **los leads se notifican de manera inmediata cuando se generan** acorde con el Lead generation funnel tu seleccionas para tu campaña. De esta manera serás capaz de usar con los datos,estadísticas, marketing automations u otro uso que necesites.

##¿Cómo funciona?

El advertiser puede instalar una URL que se llamará junto con los datos de los leads acorde con las especificaciones abajo descritas. **IMPORTANTE:** Si usas webhook para mandar recordatorios, no olvides deshabilitar “reminders” en los ajustes de campaña para evitar una superposición en las comunicaciones con tus usuarios.

## Detalles de la implementación:
Recibirá una solicitud POST codificada así  ```application/x-www-form-urlencoded``` (como un envío de formulario), con los siguientes parámetros:

|Parameter| Description|
|-------|------|
|ad_id|	l’id de la campaña|
|email|	dirección de email|
|first_name|	nombre del usuario|
|last_name|	apellido del usuario|
|gender|	género (“M” o “F”)|
|phone|	número de teléfono|
|birth_year|	año de nacimiento|
|coupon_code|	código cupón recibido por el usuario, opcional. Útil en campañas multi cupón.|
|zip_code|	código postal del usuario

Ejemplo:
```
ad_id=72&email=test%40transactionale.com&coupon_code=TRCOUPON&first_name=Marianna&zip_code=12345
```

{% include callout.html content="<strong>Nota</strong>: Los datos que recibirás depende de los datos que el publisher comparte con Transactionale. Garantizamos los campos ad_id y email. Para el resto de los campos, siempre tener presente que quizá no estén presentes. " %}

## Gestione degli errori
El contenido de la respuesta no será considerado. Los **response codes >= 300** serán considerados errores, y por lo tanto el sistema intentará enviar de nuevo la solicitud.

## Deduplica
El **HTTP 400 response code** indica que la dirección de correo electrónico está duplicada, así que no se cargará como un lead. 

