---
title: ComHelper.open method
linktitle: open method
articleTitle: open method
second_title: Aspose.Words for Python
description: "aspose.words.ComHelper.open method"
type: docs
weight: 20
url: /python-net/aspose.words/comhelper/open/
---

## open(file_name) {#str}

Allows a COM application to load a [Document](../../document/) from a file.



```python
def open(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Filename of the document to load. |

### Remarks

This method is same as calling the [Document](../../document/) constructor with a file name parameter.




### Returns

A [Document](../../document/) object that represents a Word document.


## open(stream) {#bytesio}

Allows a COM application to load [Document](../../document/) from a stream.



```python
def open(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | A .NET stream object that contains the document to load. |

### Remarks

This method is same as calling the [Document](../../document/) constructor with a stream parameter.




### Returns

A [Document](../../document/) object that represents a Word document.


## Examples

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

## See Also

* module [aspose.words](../../)
* class [ComHelper](../)

