---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific nodes effortlessly with the NodeList Item property. Retrieve nodes by index for streamlined data manipulation and efficient coding.
type: docs
weight: 20
url: /net/aspose.words/nodelist/item/
---
## NodeList indexer

Retrieves a node at the given index.

```csharp
public Node this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the list of nodes. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows how to use XPaths to navigate a NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some nodes with a DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Our document contains three Run nodes.
NodeList nodeList = doc.SelectNodes("//Run");

Assert.That(nodeList.Count, Is.EqualTo(3));
Assert.That(nodeList.Any(n => n.GetText().Trim() == "Hello world!"), Is.True);
Assert.That(nodeList.Any(n => n.GetText().Trim() == "Cell 1"), Is.True);
Assert.That(nodeList.Any(n => n.GetText().Trim() == "Cell 2"), Is.True);

// Use a double forward slash to select all Run nodes
// that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
nodeList = doc.SelectNodes("//Table//Run");

Assert.That(nodeList.Count, Is.EqualTo(2));
Assert.That(nodeList.Any(n => n.GetText().Trim() == "Cell 1"), Is.True);
Assert.That(nodeList.Any(n => n.GetText().Trim() == "Cell 2"), Is.True);

// Single forward slashes specify direct descendant relationships,
// which we skipped when we used double slashes.
Assert.That(doc.SelectNodes("//Table/Row/Cell/Paragraph/Run"), Is.EqualTo(doc.SelectNodes("//Table//Run")));

// Access the shape that contains the image we inserted.
nodeList = doc.SelectNodes("//Shape");

Assert.That(nodeList.Count, Is.EqualTo(1));

Shape shape = (Shape)nodeList[0];
Assert.That(shape.HasImage, Is.True);
```

### See Also

* class [Node](../../node/)
* class [NodeList](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
