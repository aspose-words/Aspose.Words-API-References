---
title: Forms2OleControlCollection class
linktitle: Forms2OleControlCollection class
articleTitle: Forms2OleControlCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Ole.Forms2OleControlCollection class. Represents collection of [Forms2OleControl](../forms2olecontrol/) objects"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Drawing.Ole/forms2olecontrolcollection/
---

## Forms2OleControlCollection class

Represents collection of [Forms2OleControl](../forms2olecontrol/) objects.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/nodejs-net/working-with-ole-objects/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [Forms2OleControlCollection()](./Forms2OleControlCollection/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets count of objects in the collection. |
| [this[]](./this[]/) |  |

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

* module [Aspose.Words.Drawing.Ole](../)

