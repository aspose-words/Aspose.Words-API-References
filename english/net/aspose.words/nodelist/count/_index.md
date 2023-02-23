---
title: NodeList.Count
linktitle: Count
second_title: Aspose.Words for .NET API Reference
description: NodeList property. Gets the number of nodes in the list in C#.
type: docs
weight: 10
url: /net/aspose.words/nodelist/count/
---
## NodeList.Count property

Gets the number of nodes in the list.

```csharp
public int Count { get; }
```

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

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Our document contains three Run nodes.
NodeList nodeList = doc.SelectNodes("//Run");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Use a double forward slash to select all Run nodes
// that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
nodeList = doc.SelectNodes("//Table//Run");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Single forward slashes specify direct descendant relationships,
// which we skipped when we used double slashes.
Assert.AreEqual(doc.SelectNodes("//Table//Run"), 
    doc.SelectNodes("//Table/Row/Cell/Paragraph/Run"));

// Access the shape that contains the image we inserted.
nodeList = doc.SelectNodes("//Shape");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### See Also

* class [NodeList](../)
* namespace [Aspose.Words](../../nodelist/)
* assembly [Aspose.Words](../../../)
