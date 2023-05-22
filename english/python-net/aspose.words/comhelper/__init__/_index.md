---
title: ComHelper constructor
linktitle: ComHelper constructor
articleTitle: ComHelper constructor
second_title: Aspose.Words for Python
description: "ComHelper constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /python-net/aspose.words/comhelper/__init__/
---

## ComHelper() {#default}

Initializes a new instance of this class.


```python
def __init__(self):
    ...
```

### Examples

Shows how to open documents using the ComHelper class.

```python
# The ComHelper class allows us to load documents from within COM clients.
com_helper = aw.ComHelper()

# 1 -  Using a local system filename:
doc = com_helper.open(MY_DIR + "Document.docx")

self.assertEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.get_text().strip())

# 2 -  From a stream:
with open(MY_DIR + "Document.docx", "rb") as stream:
    doc = com_helper.open(stream)
    self.assertEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ComHelper](../)

