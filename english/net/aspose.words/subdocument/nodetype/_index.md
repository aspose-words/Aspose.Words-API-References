---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: Discover the SubDocument NodeType property that efficiently returns SubDocument data, enhancing your document management and processing capabilities.
type: docs
weight: 10
url: /net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

Returns SubDocument.

```csharp
public override NodeType NodeType { get; }
```

## Examples

Shows how to access a master document's subdocument.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// This node serves as a reference to an external document, and its contents cannot be accessed.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.That(subDocument.IsComposite, Is.False);
```

### See Also

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
