---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words per .NET
description: SubDocument NodeType proprietà. RestituisceSubDocument  in C#.
type: docs
weight: 10
url: /it/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

RestituisceSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Esempi

Mostra come accedere al documento secondario di un documento master.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Questo nodo funge da riferimento a un documento esterno e non è possibile accedere al suo contenuto.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Guarda anche

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
