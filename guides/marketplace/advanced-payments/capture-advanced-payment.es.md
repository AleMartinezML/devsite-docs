---
sites_supported:
  - mla
  - mlb
  - mlm
  - mlc
  - mpe
---

# Capturar un Advanced Payment

La API de Advanced Payment permite realizar pagos del tipo [Autorización y Captura](https://www.mercadopago.com.ar/developers/es/guides/payments/api/other-features). Para estos casos se debe crear un Advanced Payment con el campo `capture` en `false`, el cual reservará el monto hasta que se capture.

Para capturarlo debes hacerlo de la siguente forma:

#### Request
```curl
curl -X PUT \
    -H 'Accept: application/json' \
    -H 'Content-Type: application/json' \
    'https://api.mercadopago.com/v1/advanced_payments/ID?access_token=MKT_ACCESS_TOKEN' \
    -d '{...}'
```

#### Body
```json
{
  "capture": true
}
```  
