---
title: Metered constructor
linktitle: Metered constructor
articleTitle: Metered constructor
second_title: Aspose.Words for Python
description: "Metered constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /de/python-net/aspose.words/metered/__init__/
---

## Metered() {#default}

Initializes a new instance of this class.


```python
def __init__(self):
    ...
```

### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# Erstellen Sie eine neue Metered-Lizenz und geben Sie anschließend deren Nutzungsstatistiken aus.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# Arbeiten Sie mit Aspose.Words und geben Sie dann erneut unsere Metered-Statistiken aus, um zu sehen, wie viel wir verbraucht haben.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# Der Aspose Metered Licensing-Mechanismus sendet die Nutzungsdaten nicht jedes Mal an den Kaufserver,
# Sie müssen warten.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

Shows how to activate a Metered license and track credit/consumption.

```python
# Erstellen Sie eine neue Metered-Lizenz und geben Sie anschließend deren Nutzungsstatistiken aus.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# Arbeiten Sie mit Aspose.Words und geben Sie dann erneut unsere Metered-Statistiken aus, um zu sehen, wie viel wir verbraucht haben.
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Der Aspose Metered Licensing-Mechanismus sendet die Nutzungsdaten nicht jedes Mal an den Kaufserver,
# Sie müssen warten.
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

