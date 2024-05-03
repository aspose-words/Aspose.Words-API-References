---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.SectionCollection class. A collection of Section objects in the document in C#.
type: docs
weight: 6000
url: /net/aspose.words/sectioncollection/
---
## SectionCollection class

A collection of [`Section`](../section/) objects in the document.

To learn more, visit the [Working with Sections](https://docs.aspose.com/words/net/working-with-sections/) documentation article.

```csharp
public class SectionCollection : NodeCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Gets the number of nodes in the collection. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Retrieves a section at the given index. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Provides a simple "foreach" style iteration over the collection of nodes. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Copies all sections from the collection to a new array of sections. (2 methods) |

## Remarks

A Microsoft Word document can contain multiple sections. To create a section in a Microsoft Word, select the Insert/Break command and select a break type. The break specifies whether section starts on a new page or on the same page.

Programmatically inserting and removing sections can be used to customize documents produced during mail merge. If a document needs to have different content or parts of the content depending on some criteria, then you can create a "master" document that contains multiple sections and delete some of the sections before or after mail merge.

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

* class [NodeCollection](../nodecollection/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
