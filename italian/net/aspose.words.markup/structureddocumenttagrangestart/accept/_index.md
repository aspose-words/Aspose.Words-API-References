---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Scopri come il metodo StructuredDocumentTagRangeStart Accept migliora l'elaborazione dei documenti accettando in modo efficace i visitatori per un'integrazione perfetta.
type: docs
weight: 200
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà i nodi. |

### Valore di ritorno

Vero se tutti i nodi sono stati visitati; falso se[`DocumentVisitor`](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.

## Osservazioni

Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama un metodo corrispondente su[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Per maggiori informazioni, vedere il design pattern Visitor.

### Guarda anche

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
