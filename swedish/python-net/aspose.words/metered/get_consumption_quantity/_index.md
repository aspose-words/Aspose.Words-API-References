---
title: Metered.get_consumption_quantity method
linktitle: get_consumption_quantity method
articleTitle: get_consumption_quantity method
second_title: Aspose.Words for Python
description: "Metered.get_consumption_quantity method. Gets consumption file size"
type: docs
weight: 30
url: /sv/python-net/aspose.words/metered/get_consumption_quantity/
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

Shows how to activate a Metered license and track credit/consumption.

```python
# Skapa en ny Metered-licens och skriv sedan ut dess användningsstatistik.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# Arbeta med Aspose.Words och skriv sedan ut våra mätade statistik igen för att se hur mycket vi har spenderat.
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Aspose Metered Licensing-mekanismen skickar inte användningsdata till inköpsservern varje gång,
# du måste vänta.
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

