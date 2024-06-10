---
title: Metered.get_consumption_credit method
linktitle: get_consumption_credit method
articleTitle: get_consumption_credit method
second_title: Aspose.Words for Python
description: "Metered.get_consumption_credit method. Gets consumption credit"
type: docs
weight: 20
url: /python-net/aspose.words/metered/get_consumption_credit/
---

## get_consumption_credit() {#default}

Gets consumption credit


```python
def get_consumption_credit(self):
    ...
```

### Returns

consumption quantity


### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# Create a new Metered license, and then print its usage statistics.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
# you need to use waiting.
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

