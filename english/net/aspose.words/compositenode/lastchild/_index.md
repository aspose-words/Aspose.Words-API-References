---
title: CompositeNode.LastChild
linktitle: LastChild
second_title: Aspose.Words for .NET API Reference
description: CompositeNode LastChild property. Gets the last child of the node in C#.
type: docs
weight: 60
url: /net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Gets the last child of the node.

```csharp
public Node LastChild { get; }
```

## Remarks

If there is no last child node, a `null` is returned.

## Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Both sections are siblings of each other.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Remove a section based on its sibling relationship with another section.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// The section we removed was the first one, leaving the document with only the second.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
