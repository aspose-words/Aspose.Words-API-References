---
title: Metered.get_consumption_credit method
linktitle: get_consumption_credit method
articleTitle: get_consumption_credit method
second_title: Aspose.Words for Python
description: "Metered.get_consumption_credit method. Gets consumption credit"
type: docs
weight: 20
url: /tr/python-net/aspose.words/metered/get_consumption_credit/
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
# Yeni bir Metered lisansı oluşturun ve ardından kullanım istatistiklerini yazdırın.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# Aspose.Words kullanarak çalışın ve ne kadar harcadığımızı görmek için metered istatistiklerimizi tekrar yazdırın.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# Aspose Metered Lisanslama mekanizması, kullanım verilerini her seferinde satın alma sunucusuna göndermez,
# beklemeniz gerekir.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

Shows how to activate a Metered license and track credit/consumption.

```python
# Yeni bir Metered lisansı oluşturun ve ardından kullanım istatistiklerini yazdırın.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# Aspose.Words kullanarak çalışın ve ne kadar harcadığımızı görmek için metered istatistiklerimizi tekrar yazdırın.
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Aspose Metered Lisanslama mekanizması, kullanım verilerini her seferinde satın alma sunucusuna göndermez,
# beklemeniz gerekir.
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

