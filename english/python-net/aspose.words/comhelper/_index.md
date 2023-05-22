---
title: ComHelper class
linktitle: ComHelper class
articleTitle: ComHelper class
second_title: Aspose.Words for Python
description: "aspose.words.ComHelper class. Provides methods for COM clients to load a document into Aspose.Words."
type: docs
weight: 150
url: /python-net/aspose.words/comhelper/
---

## ComHelper class

Provides methods for COM clients to load a document into Aspose.Words.


Use the [ComHelper](./) class to load a document from a file or stream into a 
[Document](../document/) object in a COM application.

The [Document](../document/) class provides a default constructor to create a new document
and also provides overloaded constructors to load a document from a file or stream.
If you are using Aspose.Words from a .NET application, you can use all of the [Document](../document/)
constructors directly, but if you are using Aspose.Words from a COM application,
only the default [Document](../document/) constructor is available.




### Constructors
| Name | Description |
| --- | --- |
| [ComHelper()](./__init__/#default) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ open(file_name)](./open/#str) | Allows a COM application to load a [Document](../document/) from a file. |
|[ open(stream)](./open/#bytesio) | Allows a COM application to load [Document](../document/) from a stream. |

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

* module [aspose.words](../)

