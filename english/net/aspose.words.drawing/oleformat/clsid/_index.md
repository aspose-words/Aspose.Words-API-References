---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words for .NET
description: Discover the OleFormat Clsid property to easily retrieve the CLSID of OLE objects, enhancing your application's functionality and performance.
type: docs
weight: 20
url: /net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Gets the CLSID of the OLE object.

```csharp
public Guid Clsid { get; }
```

## Examples

Shows how to access an OLE control embedded in a document and its child controls.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Shapes store and display OLE objects in the document's body.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Some OLE controls may contain child controls, such as the one in this document with three options buttons.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### See Also

* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
