# STORE LIST:

## Configurazione componente
- **api-url**: url dal quale vengono presi i dati degli stores in formato JSON (nel caso di PINKO vengono da un code resource presente in Marketing Cloud)
```
api-url="http://mypinko.pinko.com/stores"
```
- **filter-options**: oggetto di opzioni per i filtri. Se non presente non verranno visualizzati i filtri e verranno mostrati tutti gli stores.
  - è possibile cambiare placeholder, se non inserito si vedrà il placeholder che di default è in inglese
  - è possibile preselezionare una regione o una città o entrambe
```
filter-options='
{
  "region": {
    "placeholder": "Tutte le regioni",
    "preselected": "Lombardia"
  },
  "city": {
    "placeholder": "Tutte le città"
    "preselected": "Milano"
  }
}'
```
- **store-options**: oggetto di opzioni per il singolo store al quale posso aggiungere/modificare delle proprietà come:
	- store name: si può prependere una qualsiasi stringa come per esempio "PINKO Boutique"
	- store name: si può decidere se dopo questa stringa mandare a capo il name o meno con la prop "newLineAfterPrepend" settata a true
	- store name: si può visualizzare tutto in maiuscolo con la prop "uppercase" settata a true
	- è possibile modificare l'icona lei links inserendo un url a piacere, se non verrà inserito non si vedrà l'icona
```
store-options='
{
  "store name": {
    "prepend": "PINKO Boutique",
    "newLineAfterPrepend": true,
    "uppercase": true
  },
  "maps": {
    "icon": "http://image.marketing.ext.pinko.it/lib/fe8b13727663017b73/m/12/7c449ec9-0c20-4a0d-94eb-d87b762ec48b.png"
  },
  "whatsapp link": {
    "icon": "http://image.marketing.ext.pinko.it/lib/fe8b13727663017b73/m/12/09605836-f63c-4004-9268-5fb93a6aaf70.png"
  },
  "mail": {
    "icon": "http://image.marketing.ext.pinko.it/lib/fe8b13727663017b73/m/12/9358edaf-ee6a-4b07-95bc-29cda6ca2eb5.png"
  }
}'
```
## Configurazione stile
È possibile modificare il colore primario o il colore delle cards in base allo store type semplicemente modificando lo `<style>` nell'html in cui è presente il componente
- Sovrascrivere il colore primario:
```
<style>
:root {
  --und-primary-500: #cf0172  !important;
}
</style>
```

- Sovrascrivere il colore in base allo `store type`:
```
<style>
und-store-card {
  --und-store-card-color: green !important;
}
und-store-card.store-card--partner {
  --und-store-card-color: yellow !important;
}
und-store-card.store-card--owner {
  --und-store-card-color: blue !important;
}
und-store-card.store-card--newOneExample {
  --und-store-card-color: violet !important;
}
</style>
```
