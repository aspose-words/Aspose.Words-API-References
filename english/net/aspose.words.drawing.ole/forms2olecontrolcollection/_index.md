---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Ole.Forms2OleControlCollection class, your solution for managing Forms2OleControl objects efficiently in document processing.
type: docs
weight: 1470
url: /net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Represents collection of [`Forms2OleControl`](../forms2olecontrol/) objects.

To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) documentation article.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Constructors

| Name | Description |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Gets count of objects in the collection. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Gets [`Forms2OleControl`](../forms2olecontrol/) object at a specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Gets enumerator. |

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

* class [Forms2OleControl](../forms2olecontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
