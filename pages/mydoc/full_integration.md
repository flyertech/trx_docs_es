---
title: Full integration
sidebar: mydoc_sidebar
permalink: full_integration.html
folder: mydoc
---

### Overview
{% include_relative partials/integration_overview.md %}

### Where should you implement the code?
First, you have to insert the loader [as described here.](snippet_loader.html)

Then, you should implement the snippet in the following pages:

- [Home page](#home-page)
- [Products List](#products-list)
- [Product details](#product-details)
- [Shopping Basket](#shopping-basket)
- [Order Confirmation Page](#order-confirmation-page)

You can also implement the [lead-webhook](#receiving-leads) to receive leads in real-time.

### Home page 
The [home page snippet](snippet_homepage.md) allows monitoring the so-called *bounces*: users that land on the website and then leave without shopping.

### Products list
Any page in the catalog that shows a list of products - i.e. a category page, or search results, or a brand's page.
The [products list snippet](snippet_pagina_ricerca.md) allows monitoring of user interests toward certain products or categories.

Many users only browse categories or search results, without clicking on any detail page, so this implementation is key to monitor these users.

### Product details
The product page shows details of a single product. Installing the [product page snippet](snippet_pagina_prodotto.md) is extremely important because it can track a users's clear interest in a product. Many users directly land on product pages without going through categories or search.

### Shopping basket
The [shopping basket snippet](snippet_carrello.md) allows monitoring users close to conversion, but do not complete the order process.

### Order confirmation page
When a user completes a purchase on your website, he/she will usually be shown a confirmation page containing the order ID and its contents.
By implementing the [confirmation page snippet](snippet_pagina_conferma.md) we will track the products your users have bought.

Monitoring purchases allows optimizing the distribution of targeted offers and avoids showing users products they already purchased.

### Receiving leads
It is possible to receive **in real time** the data of generated leads to channel them into automation flows, like **newsletters**, **email automation** systems or more.
This is also required to allow **deduplication** of leads, to avoid paying for contacts you already possess.

Please read the details in the [webhook](webhook.html) section.

### Optional or custom integrations
TODO

### Generic page view
TODO

### Custom lead-generation events
TODO

### Manually sending a promotional email
TODO




