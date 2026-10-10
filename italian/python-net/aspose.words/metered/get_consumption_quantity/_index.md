---
title: Metered.get_consumption_quantity method
linktitle: get_consumption_quantity method
articleTitle: get_consumption_quantity method
second_title: Aspose.Words for Python
description: "Metered.get_consumption_quantity method. Gets consumption file size"
type: docs
weight: 30
url: /it/python-net/aspose.words/metered/get_consumption_quantity/
---

## get_consumption_quantity() {#default}

Gets consumption file size


```python
def get_consumption_quantity(self):
    ...
```

### Returns

consumption quantity


### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# Crea una nuova licenza Metered e poi stampa le sue statistiche di utilizzo.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# Operare usando Aspose.Words e poi stampare di nuovo le nostre statistiche metered per vedere quanto abbiamo speso.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# Il meccanismo di licenza Aspose Metered non invia i dati di utilizzo al server di acquisto ogni volta,
# è necessario attendere.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

Shows how to activate a Metered license and track credit/consumption.

```python
# Crea una nuova licenza Metered e poi stampa le sue statistiche di utilizzo.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# Operare usando Aspose.Words e poi stampare di nuovo le nostre statistiche metered per vedere quanto abbiamo speso.
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Il meccanismo di licenza Aspose Metered non invia i dati di utilizzo al server di acquisto ogni volta,
# è necessario attendere.
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

