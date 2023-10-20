---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words pour .NET
description: SubDocument NodeType propriété. RetoursSubDocument  en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

RetoursSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Exemples

Montre comment accéder au sous-document d’un document maître.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Ce nœud sert de référence à un document externe et son contenu n'est pas accessible.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Voir également

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
