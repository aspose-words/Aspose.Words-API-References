---
title: SubDocument.NodeType
second_title: Aspose.Words per .NET API Reference
description: SubDocument proprietà. Restituisce NodeType.SubDocument
type: docs
weight: 10
url: /it/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

Restituisce **NodeType.SubDocument**

```csharp
public override NodeType NodeType { get; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../subdocument/)
* assemblea [Aspose.Words](../../../)


