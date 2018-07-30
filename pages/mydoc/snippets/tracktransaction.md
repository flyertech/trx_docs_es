```js
window._trx.push(
    {
        event: 'trackTransaction',
        transaction: {
            id: 'xxxxx', // número de orden
            subtotal: xxx.xx,
            shipping: xxx.xx,
            discount: xxx.xx,
            total: xxx.xx, // requerido
            coupon: 'xxx', 
            currency: 'EUR', // EUR por default
        },
        items: [
            {id: x, price: xx.xx, quantity: x}, 
            {id: x, price: xx.xx, quantity: x},
        ],
        address: {
            address: 'xxxxxx',
            address2: 'xxxxxx',
            city: 'xxxxx',
            postalCode: 'xxxxx',
            country: 'ES',
            phone: 'xxxxxxxx',
            phoneMobile: 'xxxxxxxxx',
        },
        customer: {
            firstName: 'Xxxxx',
            lastName: 'Xxxxxxx',
            company: 'xxxxxxxx',
            email: 'xxxxx@xxxx.xx',
            birthDate: 'yyyy-mm-dd',
            gender: 'x', // M o F
            optin: xxxx // si los usuarios optan por recibir ofertas comerciales
        },
          // ejemplo de integración de ads directamente en la página web
        touchpointType: 'auto', 
    }
);
```
```html
<div id="tr_touchpoint_container"></div>
```