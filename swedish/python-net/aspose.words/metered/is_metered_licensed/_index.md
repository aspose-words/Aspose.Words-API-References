---
title: Metered.is_metered_licensed method
linktitle: is_metered_licensed method
articleTitle: is_metered_licensed method
second_title: Aspose.Words for Python
description: "Metered.is_metered_licensed method. Check whether metered is licensed"
type: docs
weight: 50
url: /sv/python-net/aspose.words/metered/is_metered_licensed/
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
# Skapa en ny Metered-licens och skriv sedan ut dess användningsstatistik.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# Arbeta med Aspose.Words och skriv sedan ut våra mätade statistik igen för att se hur mycket vi har spenderat.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# Aspose Metered Licensing-mekanismen skickar inte användningsdata till inköpsservern varje gång,
# du måste vänta.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

