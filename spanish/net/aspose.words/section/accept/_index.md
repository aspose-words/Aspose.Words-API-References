---
title: Section.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words para .NET
description: Section Accept método. Acepta un visitante en C#.
type: docs
weight: 70
url: /es/net/aspose.words/section/accept/
---
## Section.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará los nodos. |

### Valor_devuelto

Verdadero si se visitaron todos los nodos; falso si[`DocumentVisitor`](../../documentvisitor/) detuvo la operación antes de visitar todos los nodos.

## Observaciones

Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en[`DocumentVisitor`](../../documentvisitor/).

Para obtener más información, consulte el patrón de diseño Visitante.

llamadas[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , luego llama[`Accept`](../../node/accept/) para todos los nodos secundarios de la sección y llamadas[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) al final.

### Ver también

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
