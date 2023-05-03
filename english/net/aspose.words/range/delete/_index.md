---
title: Range.Delete
linktitle: Delete
second_title: Aspose.Words for .NET API Reference
description: Range Delete method. Deletes all characters of the range in C#.
type: docs
weight: 70
url: /net/aspose.words/range/delete/
---
## Range.Delete method

Deletes all characters of the range.

```csharp
public void Delete()
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

* class [Range](../)
* namespace [Aspose.Words](../../range/)
* assembly [Aspose.Words](../../../)
