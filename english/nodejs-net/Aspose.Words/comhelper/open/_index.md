---
title: ComHelper.open method
linktitle: open method
articleTitle: open method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ComHelper.open method"
type: docs
weight: 20
url: /nodejs-net/aspose.words/comhelper/open/
---

## open(fileName) {#string}

Allows a COM application to load a [Document](../../document/) from a file.



```js
open(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | Filename of the document to load. |

### Remarks

This method is same as calling the [Document](../../document/) constructor with a file name parameter.




### Returns

A [Document](../../document/) object that represents a Word document.


## open(stream) {#buffer}

Allows a COM application to load [Document](../../document/) from a stream.



```js
open(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | A .NET stream object that contains the document to load. |

### Remarks

This method is same as calling the [Document](../../document/) constructor with a stream parameter.




### Returns

A [Document](../../document/) object that represents a Word document.


## Examples

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

## See Also

* module [Aspose.Words](../../)
* class [ComHelper](../)

