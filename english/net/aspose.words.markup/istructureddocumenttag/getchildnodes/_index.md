---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words for .NET
description: IStructuredDocumentTag GetChildNodes method. Returns a live collection of child nodes that match the specified types in C#.
type: docs
weight: 160
url: /net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Returns a live collection of child nodes that match the specified types.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
