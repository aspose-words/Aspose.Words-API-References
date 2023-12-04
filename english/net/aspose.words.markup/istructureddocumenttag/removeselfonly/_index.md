---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words for .NET
description: IStructuredDocumentTag RemoveSelfOnly method. Removes just this SDT node itself but keeps the content of it inside the document tree in C#.
type: docs
weight: 170
url: /net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Removes just this SDT node itself, but keeps the content of it inside the document tree.

```csharp
public void RemoveSelfOnly()
```

## Examples

Shows how to remove structured document tag, but keeps content inside.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// This collection provides a unified interface for accessing ranged and non-ranged structured tags. 
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.Cast<IStructuredDocumentTag>().ToList();
Assert.AreEqual(5, sdts.Count());

// Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
foreach (IStructuredDocumentTag sdt in sdts)                
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.Cast<IStructuredDocumentTag>().ToList();
Assert.AreEqual(0, sdts.Count());
```

### See Also

* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
