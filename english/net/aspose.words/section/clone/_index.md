---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Section Clone method. Creates a duplicate of this section in C#.
type: docs
weight: 110
url: /net/aspose.words/section/clone/
---
## Section.Clone method

Creates a duplicate of this section.

```csharp
public Section Clone()
```

## Examples

Shows how to add and remove sections in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Delete the first section from the document.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Append a copy of what is now the first section to the end of the document.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
