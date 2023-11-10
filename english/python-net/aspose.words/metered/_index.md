---
title: Metered class
linktitle: Metered class
articleTitle: Metered class
second_title: Aspose.Words for Python
description: "aspose.words.Metered class. Provides methods to set metered key."
type: docs
weight: 710
url: /python-net/aspose.words/metered/
---

## Metered class

Provides methods to set metered key.


### Constructors
| Name | Description |
| --- | --- |
| [Metered()](./__init__/#default) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ get_consumption_credit()](./get_consumption_credit/#default) | Gets consumption credit |
|[ get_consumption_quantity()](./get_consumption_quantity/#default) | Gets consumption file size |
|[ get_product_name()](./get_product_name/#default) |  |
|[ is_metered_licensed()](./is_metered_licensed/#default) | Check whether metered is licensed |
|[ set_metered_key(public_key, private_key)](./set_metered_key/#str_str) | Sets metered public and private key. If you purchase metered license, when start application, this API should be called, normally, this is enough.  However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status,  to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again. |

### Examples

Shows how to activate a Metered license and track credit/consumption.

```python
# Create a new Metered license, and then print its usage statistics.
metered = aw.Metered()
metered.set_metered_key("MyPublicKey", "MyPrivateKey")

print("Credit before operation:", metered.get_consumption_credit())
print("Consumption quantity before operation:", metered.get_consumption_quantity())

# Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
doc = aw.Document(MY_DIR + "Document.docx")
doc.save(ARTIFACTS_DIR + "Metered.usage.pdf")

# Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
# you need to use waiting.
time.sleep(10)

print("Credit after operation:", metered.get_consumption_credit())
print("Consumption quantity after operation:", metered.get_consumption_quantity())
```

### See Also

* module [aspose.words](../)

