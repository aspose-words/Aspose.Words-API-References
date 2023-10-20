---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: SubDocument NodeType eigendom. Gibt zurückSubDocument  in C#.
type: docs
weight: 10
url: /de/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

Gibt zurückSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Beispiele

Zeigt, wie auf das Unterdokument eines Masterdokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Dieser Knoten dient als Referenz auf ein externes Dokument und auf seinen Inhalt kann nicht zugegriffen werden.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Siehe auch

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
