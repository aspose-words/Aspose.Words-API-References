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


## See Also

* module [aspose.words](../../)
* class [ComHelper](../)

