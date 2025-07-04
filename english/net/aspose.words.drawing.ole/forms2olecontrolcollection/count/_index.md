---
title: Forms2OleControlCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the Forms2OleControlCollection Count property to easily retrieve the total number of objects in your collection for enhanced data management.
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

Assert.That(shape.OleFormat.Clsid.ToString(), Is.EqualTo("6e182020-f460-11ce-9bcd-00aa00608e01"));

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Some OLE controls may contain child controls, such as the one in this document with three options buttons.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.That(oleControlCollection.Count, Is.EqualTo(3));

Assert.That(oleControlCollection[0].Caption, Is.EqualTo("C#"));
Assert.That(oleControlCollection[0].Value, Is.EqualTo("1"));

Assert.That(oleControlCollection[1].Caption, Is.EqualTo("Visual Basic"));
Assert.That(oleControlCollection[1].Value, Is.EqualTo("0"));

Assert.That(oleControlCollection[2].Caption, Is.EqualTo("Delphi"));
Assert.That(oleControlCollection[2].Value, Is.EqualTo("0"));
```

### See Also

* class [Forms2OleControlCollection](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
