---
title: OleFormat.clsid property
linktitle: clsid property
articleTitle: clsid property
second_title: Aspose.Words for NodeJs
description: "OleFormat.clsid property. Gets the CLSID of the OLE object."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Drawing/oleformat/clsid/
---

## OleFormat.clsid property

Gets the CLSID of the OLE object.


```js
get clsid(): uuid
```

### Examples

Shows how to access an OLE control embedded in a document and its child controls.

```js
let doc = new aw.Document(base.myDir + "OLE ActiveX controls.docm");

// Shapes store and display OLE objects in the document's body.
let shape = doc.getShape(0, true);

expect(shape.oleFormat.clsid.toString().toLowerCase()).toEqual("6e182020-f460-11ce-9bcd-00aa00608e01");

let oleControl = shape.oleFormat.oleControl.asForms2OleControl();

// Some OLE controls may contain child controls, such as the one in this document with three options buttons.
let oleControlCollection = oleControl.childNodes;

expect(oleControlCollection.count).toEqual(3);

expect(oleControlCollection.at(0).caption).toEqual("C#");
expect(oleControlCollection.at(0).value).toEqual("1");

expect(oleControlCollection.at(1).caption).toEqual("Visual Basic");
expect(oleControlCollection.at(1).value).toEqual("0");

expect(oleControlCollection.at(2).caption).toEqual("Delphi");
expect(oleControlCollection.at(2).value).toEqual("0");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [OleFormat](../)

