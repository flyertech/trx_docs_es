---
title: "Integración simplificada:"
sidebar: mydoc_sidebar
permalink: simplified_integration.html
folder: mydoc
---

### Sumario general:
{% include_relative partials/integration_overview.md %}

{% include callout.html content="La integración simplificada no se aconseja para publishers ya que reduce la calidad de hacer perfiles así como el performance de la generación de leads." %}

### Pon el loader tag en todas las páginas
El loader tag va en `<head>` de tu plantilla base.

{% include_relative snippets/loader_viewPage.md %}

### Pon trackTransaction en la página de confirmación de pedido:
Este tag debe ser insertado preferiblemente antes de cerrar `</body>`, o en cualquier caso después del loader dentro del tag `<head>`. Debes rellenar tantos campos como puedas con los valores necesarios relativos a la orden presentada. 

{% include callout.html content="ATENCIÓN: el ejemplo valor (‘xxxx’) debe ser reemplazado con la correspondiente variable; puedes eliminar los campos que no desees conservar.
" %}

{% include_relative snippets/tracktransaction.md %}

### Selección del touchpoint automático
Configurando `auto` como `touchpointType`, el mejor touchpoint será activado automáticamente en concordancia con los valores aportados.En caso de que el touchpoint de la web sea activado sin aportar touchpointId, será usado el que hay por default.

### Web y auto touchpoints
Si estás usando una web (ó auto) touchpoint, debes definir dónde quieres que aparezcan las ofertas en tu página. Para hacerlo, inserta  `<div id="tr_touchpoint_container"></div>` en el lugar escogido.

### Ofertas con banner
Si quieres usar la versión banner en tu touchpoint web, tienes 2 disposiciones disponibles para elegir: Horizontal (por defecto) o vertical. 


{% include image.html file="banner_horizontal.png" url="images/banner_horizontal.png" %}

Puedes activar la disposición vertical añadiendo `tr-touchpoint-layout-vertical` class al `<div>` de esta manera:<br>
 `<div id="tr_touchpoint_container" class="tr-touchpoint-layout-vertical"></div>` <br>
El banner se verá de una manera similar a esta:

{% include image.html file="banner_vertical.png" url="images/banner_vertical.png" %}

### Verificar la integración y webhook

Puedes mirar que funcione correctamente la integración tecnológica y el webhook url a través de estas instrucciones sencillas:

{% include_relative partials/link_verify.md %}