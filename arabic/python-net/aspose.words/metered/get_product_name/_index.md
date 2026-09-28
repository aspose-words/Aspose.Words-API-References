---
title: Metered.get_product_name method
linktitle: get_product_name method
articleTitle: get_product_name method
second_title: Aspose.Words for Python
description: "Metered.get_product_name method. Returns Product name"
type: docs
weight: 40
url: /ar/python-net/aspose.words/metered/get_product_name/
---

## get_product_name() {#default}

Returns Product name


```python
def get_product_name(self):
    ...
```

### Returns

Product name


### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# أنشئ ترخيصًا مقيسًا جديدًا، ثم اطبع إحصائيات الاستخدام الخاصة به.
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# استخدم Aspose.Words، ثم اطبع إحصاءاتنا المقيسة مرة أخرى لمعرفة مقدار ما أنفقناه.
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# آلية ترخيص Aspose المقيسة لا تُرسل بيانات الاستخدام إلى خادم الشراء في كل مرة،
# تحتاج إلى الانتظار.
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

