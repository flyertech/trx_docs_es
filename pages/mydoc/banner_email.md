---
title: Banner in email
sidebar: mydoc_sidebar
permalink: banner_email.html
folder: mydoc
---

### Enviar ofertas en las propias email
Para los **Publisher habilitados**,  es posible  **insertar en los correos enviados un banner** con una oferta seleccionada automáticamente por Transactionale, para incrementar el número de las ofertas vehiculadas y la posibilidad de monetización y fidelización.  

### Caraterísticas principales
El banner email no prevé la transmisión de los datos personales a Transacitionale, por lo tanto está en **conformidad con el GDPR** sin necesidad de intervenir en los consentimientos de privacidad. <br>
**La integración es inmediata** ya que simplemente consta de una imagen con un enlace en el template de los correos enviados. 

### Activación del touchpoint
Desde la sección **Monetize -> Web Touchpoints** de tu account Transactionale, añade un nuevo touchpoint con formato  **Email Banner**:

{% include image.html file="email_banner.png" url="images/email_banner.png" %}

Se abrirá un box de detalles con dentro dos URL:

{% include image.html file="snippet_mail_banner2.png" url="images/snippet_mail_banner2.png" %}

Es posible utilizar estos dos URL para generar tag imagen a mano o, cliqueando sobre el botón Snippet es disponible un tag de ejemplo, listo para pegar.

{% include callout.html content="IMPORTANTE: es necesario  **personalizar los URL** antes del utilizo" %}

### Personalización de los URL
Para garantizar el funcionamiento del touchpoint, es necesario substituir la parte **{transaction_id}**  de los dos URL con una variable unívoca para cada correo enviado, por ejemplo el número de pedido.Verificar como utilizar las variables en la documentación de la propia plataforma. 
Ejemplo:
```html
https://www.transactionale.com/m/xxxxxx/yyy/b?transaction_id={ $order->id }&zip_code={ $zip_code }&gender={ $gender }
```

Si se quiere insertar el banner en más de un tipo de correo, teniendo el mismo transaction_id, se aconseja utilizar un prefijo para distinguir los contenidos, por ejemplo:
```html
https://www.transactionale.com/m/xxxxxx/yyy/b?transaction_id={ $order->id }&zip_code={ $zip_code }&gender={ $gender }

```

{% include callout.html content="IMPORTANTE:  el valor del campo **transaction_id** tiene que ser igual en ambos URL" %}


### Posicionamiento del banner
Es posible **insertar el banner en cada zona del correo**,  garantizando que pueda ocupar el 100% del ancho del layout, por ejemplo insertando **el estilo en el tag:**

```html
<a href="https://www.transactionale.com/m/xxxxxx/yyy/click?transaction_id={transaction_id}}&zip_code={ $zip_code }&gender={ $gender }" target="_blank">
  <img src="https://www.transactionale.com/m/xxxxxx/yyy/b?transaction_id={transaction_id}}&zip_code={ $zip_code }&gender={ $gender }" style="width: 100%">
</a>
```