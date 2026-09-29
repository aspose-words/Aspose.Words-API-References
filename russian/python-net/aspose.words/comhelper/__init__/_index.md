---
title: ComHelper constructor
linktitle: ComHelper constructor
articleTitle: ComHelper constructor
second_title: Aspose.Words for Python
description: "ComHelper constructor. Initializes a new instance of this class."
type: docs
weight: 10
url: /ru/python-net/aspose.words/comhelper/__init__/
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
# Класс **ComHelper** позволяет нам загружать документы из COM‑клиентов.
com_helper = aw.ComHelper()
# 1 -  Использование локального системного имени файла:
doc = com_helper.open(file_name=MY_DIR + 'Document.docx')
self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
# 2 -  Из потока:
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream:
    doc = com_helper.open(stream=stream)
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ComHelper](../)

