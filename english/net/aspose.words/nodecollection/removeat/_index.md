---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
second_title: Aspose.Words for .NET API Reference
description: NodeCollection RemoveAt method. Removes the node at the specified index from the collection and from the document in C#.
type: docs
weight: 100
url: /net/aspose.words/nodecollection/removeat/
---
## RemoveAt method

Removes the node at the specified index from the collection and from the document.

```csharp
public void RemoveAt(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

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

* class [NodeCollection](../)
* namespace [Aspose.Words](../../nodecollection/)
* assembly [Aspose.Words](../../../)
