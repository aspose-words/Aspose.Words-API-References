---
title: Metered.get_product_name method
linktitle: get_product_name method
articleTitle: get_product_name method
second_title: Aspose.Words for Python
description: "Metered.get_product_name method. Returns Product name"
type: docs
weight: 40
url: /zh/python-net/aspose.words/metered/get_product_name/
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
# 创建一个新的 Metered 许可证，然后打印其使用统计信息。
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print(f'Is metered license accepted: {aw.Metered.is_metered_licensed()}')
print(f'Product name: {metered.get_product_name()}')
print(f'Credit before operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity before operation: {aw.Metered.get_consumption_quantity()}')
# 使用 Aspose.Words 操作，然后再次打印我们的计量统计以查看花费了多少。
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Metered.Usage.pdf')
# Aspose 计量授权机制不会每次都将使用数据发送到购买服务器，
# 您需要等待。
time.sleep(10)
print(f'Credit after operation: {aw.Metered.get_consumption_credit()}')
print(f'Consumption quantity after operation: {aw.Metered.get_consumption_quantity()}')
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

