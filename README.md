# DOCUMENTAZIONE STORE LIST:

- **api-url**: url dal quale vengono presi i dati degli stores in formato JSON (nel caso di PINKO vengono da un code resource presente in Marketing Cloud)
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
	- è possibile modificare l'icona di maps e di whatsapp inserendo un url a piacere, se non verrà inserito non si vedrà l'icona
```
	store-options='
		{
		  "store name": {
		    "prepend": "PINKO Boutique",
		    "newLineAfterPrepend": true
		  },
		  "maps": {
		    "icon": "http://image.marketing.ext.pinko.it/lib/fe8b13727663017b73/m/12/7c449ec9-0c20-4a0d-94eb-d87b762ec48b.png"
		  },
		  "whatsapp link": {
		    "icon": "http://image.marketing.ext.pinko.it/lib/fe8b13727663017b73/m/12/09605836-f63c-4004-9268-5fb93a6aaf70.png"
		  }
		}'
```
