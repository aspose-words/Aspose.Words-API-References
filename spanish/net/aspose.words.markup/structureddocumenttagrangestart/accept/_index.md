---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words para .NET
description: StructuredDocumentTagRangeStart Accept método. Acepta un visitante en C#.
type: docs
weight: 190
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará los nodos. |

### Valor_devuelto

Verdadero si se visitaron todos los nodos; falso si[`DocumentVisitor`](../../../aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.

## Observaciones

Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Para obtener más información, consulte el patrón de diseño Visitante.

### Ver también

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
