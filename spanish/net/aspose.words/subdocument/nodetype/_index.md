---
title: SubDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: SubDocument NodeType propiedad. DevolucionesSubDocument  en C#.
type: docs
weight: 10
url: /es/net/aspose.words/subdocument/nodetype/
---
## SubDocument.NodeType property

DevolucionesSubDocument .

```csharp
public override NodeType NodeType { get; }
```

## Ejemplos

Muestra cómo acceder al subdocumento de un documento maestro.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Este nodo sirve como referencia a un documento externo y no se puede acceder a su contenido.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Ver también

* enum [NodeType](../../nodetype/)
* class [SubDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
