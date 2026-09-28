---
title: Metered.set_metered_key method
linktitle: set_metered_key method
articleTitle: set_metered_key method
second_title: Aspose.Words for Python
description: "Metered.set_metered_key method. Sets metered public and private key"
type: docs
weight: 60
url: /zh/python-net/aspose.words/metered/set_metered_key/
---

## set_metered_key(public_key, private_key) {#str_str}

Sets metered public and private key.
If you purchase metered license, when start application, this API should be called, normally, this is enough. 
However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status, 
to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again.


```python
def set_metered_key(self, public_key: str, private_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| public_key | str | public key |
| private_key | str | private key |

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

Shows how to activate a Metered license and track credit/consumption.

```python
# 创建一个新的 Metered 许可证，然后打印其使用统计信息。
metered = aw.Metered()
metered.set_metered_key('MyPublicKey', 'MyPrivateKey')
print('Credit before operation:', metered.get_consumption_credit())
print('Consumption quantity before operation:', metered.get_consumption_quantity())
# 使用 Aspose.Words 操作，然后再次打印我们的计量统计以查看花费了多少。
doc = aw.Document(MY_DIR + 'Document.docx')
doc.save(ARTIFACTS_DIR + 'Metered.usage.pdf')
# Aspose 计量授权机制不会每次都将使用数据发送到购买服务器，
# 您需要等待。
time.sleep(10)
print('Credit after operation:', metered.get_consumption_credit())
print('Consumption quantity after operation:', metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../../)
* class [Metered](../)

