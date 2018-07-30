---
title:  "Cómo instalar y configurar el módulo de Prestashop >= 1.6"
permalink: prestashop16.html
sidebar: mydoc_sidebar
folder: mydoc
---


### Obtener el último módulo de Prestashop:
Puedes descargarte la última versión desde tu dashboard yendo a  **My Account -> Integration -> Select Prestashop <= 1.6**, click  **Download the plugin**

{% include image.html file="prestashop16/downloadplugin.png" url="images/prestashop16/downloadplugin.png" %}

### Instalar el módulo:
Ve a tu Prestashop **Módulos y Servicios**  haz click en **Añadir nuovo módulo**.. Aparecerá un formulario donde puedes subir el archivo zip del módulo, clicka en **Elegin un fichero** y  **Subir este módulo**.

{% include image.html file="prestashop16/1.png" url="images/prestashop16/1.png" %}

Aparecerá la lista de los módulos, y en particular el módulo Transactionale recién subido.Tienes que hacer click en **Instalar**.

{% include image.html file="prestashop16/2.png" url="images/prestashop16/2.png" %}

Aparecerá un popup, haz click en **Seguir con la instalación**

{% include image.html file="prestashop16/3.png" url="images/prestashop16/3.png" %}

### Detalles de ajuste:
Serás redirigido a la página del módulo de configuración:
{% include image.html file="prestashop16/4.png" url="images/prestashop16/4.png" %}

Los detalles de los campos desplegados se muestran a continuación:

*Auth Key*|Se usa para identificar tu cuenta. **Sigue las instrucciones más abajo para rellenarlo**.
*Country*|de dos letras ISO para el país en el que tu tienda opera. IT, ES.
*Touchpoint Type*|Cómo entregar las ofertas a los clientes. Asegúrate de que configuras los touchpoints en tu cuenta de Transactionale. Puede ser Web, Mail, Web+Mail.
*Web Touchpoint Id*|Si usas touchpoint web, puedes especificar un ID, sino, se usará el ID que está por default.
*Web Touchpoint Text*|Si usas web touchpoint descrito arriba, puedes especificar el texto que quieres que se muestre en la oferta.
*Import leads automatically*|Habilita la importación automática de leads. Cuando habilitado, copia y pega URL desplegado en tu cuenta de Transactionale así: My Account -> Integration -> Webhook URL.

{% include image.html file="prestashop16/5.png" url="images/prestashop16/5.png" %}

### Habilitar/ Deshabilitar el Optin
El opt-in debe ser activado desde la sección **Preferencias -> Clientes**.
{% include image.html file="prestashop16/optin.png" url="images/prestashop16/optin.png" %}

### Ultimi step

Copia tu Auth Key desde tu cuenta de Transactionale dalla sezione **My Account-> Integration** pega en Auth Key del módulo de configuración de Prestashop.

{% include image.html file="prestashop16/apikey.png" url="images/prestashop16/apikey.png" %}

Recuerda guardar todos los cambios.


### Habilitar la importación automática de leads - Webhook


ara la importación automática de leads via webhook, has de seleccionar  **Sí** en el campo **Import leads automatically**

{% include image.html file="prestashop16/webhook.png" url="images/prestashop16/webhook.png" %}

Copia el link que ves en la sección  **My Account-> Integration** de tu cuenta Transactionale en el campo **Webhook Url**

{% include image.html file="prestashop16/webhookurl.png" url="images/prestashop16/webhookurl.png" %}

### Verifica la integración y webhook

Puedes verificar la el correcto funcionamiento de la integración tecnológica y el URL Webhook a través de estas simples instrucciones:

{% include_relative partials/link_verify.md %}