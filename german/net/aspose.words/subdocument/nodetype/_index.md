---
title: SubDocument.NodeType
second_title: Aspose.Words für .NET-API-Referenz
description: SubDocument eigendom. gibt zurück NodeType.SubDocument
type: docs
weight: 10
url: /de/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

gibt zurück **NodeType.SubDocument**

```csharp
public override NodeType NodeType { get; }
```

### Beispiele

Zeigt, wie auf das Filialdokument eines Globaldokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Dieser Knoten dient als Verweis auf ein externes Dokument, auf dessen Inhalt nicht zugegriffen werden kann.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Siehe auch

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* namensraum [Aspose.Words](../../subdocument/)
* Montage [Aspose.Words](../../../)


