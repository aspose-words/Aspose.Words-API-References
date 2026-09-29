---
title: Metered.is_metered_licensed method
linktitle: is_metered_licensed method
articleTitle: is_metered_licensed method
second_title: Aspose.Words for Python
description: "Metered.is_metered_licensed method. Check whether metered is licensed"
type: docs
weight: 50
url: /es/python-net/aspose.words/metered/is_metered_licensed/
---

## is_metered_licensed() {#default}

Check whether metered is licensed


```python
def is_metered_licensed(self):
    ...
```

### Returns

True or false


### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# Crea una nueva licencia Metered y luego imprime sus estadísticas de uso.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# Opera usando Aspose.Words y luego imprime nuestras estadísticas de licencia Metered nuevamente para ver cuánto gastamos.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# El mecanismo de licenciamiento Metered de Aspose no envía los datos de uso al servidor de compra cada vez,
# es necesario usar espera.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

