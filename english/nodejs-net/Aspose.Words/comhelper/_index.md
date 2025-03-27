---
title: ComHelper class
linktitle: ComHelper class
articleTitle: ComHelper class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.ComHelper class. Provides methods for COM clients to load a document into Aspose.Words."
type: docs
weight: 180
url: /nodejs-net/Aspose.Words/comhelper/
---

## ComHelper class

Provides methods for COM clients to load a document into Aspose.Words.


### Remarks

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
| [ComHelper()](./ComHelper/#default) | Initializes a new instance of this class. |

### Methods

| Name | Description |
| --- | --- |
|[ open(fileName)](./open/#string) | Allows a COM application to load a [Document](../document/) from a file. |
|[ open(stream)](./open/#buffer) | Allows a COM application to load [Document](../document/) from a stream. |

### Examples

Shows how to open documents using the ComHelper class.

```js
// The ComHelper class allows us to load documents from within COM clients.
let comHelper = new aw.ComHelper();

// 1 -  Using a local system filename:
let doc = comHelper.open(base.myDir + "Document.docx");

expect(doc.getText().trim()).toEqual("Hello World!\r\rHello Word!\r\r\rHello World!");

// 2 -  From a stream:
let stream = base.loadFileToBuffer(base.myDir + "Document.docx");
doc = comHelper.open(stream);
expect(doc.getText().trim()).toEqual("Hello World!\r\rHello Word!\r\r\rHello World!");
```

### See Also

* module [Aspose.Words](../)

