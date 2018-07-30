---
title: "Visión General"
sidebar: mydoc_sidebar
permalink: index.html
folder: mydoc
summary: Detalles de la integración V2 

---

Esta es la documentación técnica de Transactionale donde puedes encontrar todos los detalles para poder integrar tu e-shop con Transactionale.

# ¿Cómo hacerlo? Instrucciones técnicas:

Os podéis integrar de una manera muy simple:

  - [Full integration](full_integration.html), **recomendado** para una mejor rendimiento (versión en inglés),
  - [Integración simplificada](simplified_integration.html) .

E' possibile attivare la [modalità di sviluppo](debugging.html) per verificare la correttezza dell'integrazione.

# Cómo funciona el network

## Advertiser {#advertiser}
Con **Transactionale** podrás atraer nuevos clientes potenciales en tu e-shop y traquear sus conversiones.

### Cómo atraigo a nuevos clientes?
En sólo unos pasos, serás capaz de crear una **campaña de publicidad**y nosotros **la distribuiremos en nuestro network**. Los clientes de otras tiendas recibirán tu oferta y querrán hacer uso de ella en tu página web. Esto te permitirá adquirir Leads cualificados de clientes reales que compran online.

Si también eliges ser [publisher](#publisher), puedes **monetizar**, y  reinvertir las ganancias en campañas de adquisición de leads cualificados, disminuyendo su coste. 

### Cómo gestionar los leads generados:
Nosotros llevamos un registro de todos los leads generados, permitiéndole monitorizar en su plataforma cómo están performando las campañas.

A la vez podemos enviar cada lead generado en tu sistema en **tiempo real** para permitirte coleccionar todos los datos de los **leads generados** directamente en tu plataforma.Esto permite integraciones con **newsletters**, sistemas de **email automation**, remarketing y más. Ve a la sección de [webhook](webhook.html) para los detalles de la implementación. El uso de webhook es requerido para habilitar el sistema de **deduplication**.

## Publisher {#publisher}
Con **Transactionale** serás capaz de monetizar gracias a tus clientes al mismo tiempo que premias ofreciéndoles ofertas especiales targuetizadas.

### Cómo gano a través del network?
Cuando Lisa, uno de tus clientes, **finaliza una compra en tu eshop**, Transactionale le enviará unas ofertas de otras tiendas de la red- Complementarias, no competencia- Cada vez que una oferta genera un lead, ( que es cuando Lisa hace click en la oferta y aterriza en la web del advertiser) tú, **ganas dinero**.

Además, si eres [advertiser](#advertiser), puedes reinvertir tus ganancias en campañas de adquisición de leads cualificados bajando los costes de las mismas.

### Cómo funciona?
1. Lisa hace una orden en tu eshop,
2. Cada vez que se **finaliza una orden**, tu tienda **nos lo notifica** a través de un **snippet de trackeo**, normalmente **en la thank you page**,
3. Tan pronto como Transactionale recibe la notificación, mandará a Lisa el **email Transactionale** con ofertas targuetizadas,
4. Si Lisa hace click en la oferta, se genera un **lead**.

