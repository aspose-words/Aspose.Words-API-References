---
title: Count
second_title: Aspose.Words for .NET API Reference
description: Forms2OleControlCollection property. Gets count of objects in the collection in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

Gets count of objects in the collection.

```csharp
public int Count { get; }
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

* class [Forms2OleControlCollection](../)
* namespace [Aspose.Words.Drawing.Ole](../../forms2olecontrolcollection/)
* assembly [Aspose.Words](../../../)
