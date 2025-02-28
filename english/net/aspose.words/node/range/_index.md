---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words for .NET
description: Discover the Node Range property: effortlessly access a Range object that defines the document segment within your node for enhanced content management.
type: docs
weight: 80
url: /net/aspose.words/node/range/
---
## Node.Range property

Returns a [`Range`](../../range/) object that represents the portion of a document that is contained in this node.

```csharp
public Range Range { get; }
```

## Examples

Shows how to delete all the nodes from a range.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text to the first section in the document, and then add another section.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Remove the first section entirely by removing all the nodes
// within its range, including the section itself.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### See Also

* class [Range](../../range/)
* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
