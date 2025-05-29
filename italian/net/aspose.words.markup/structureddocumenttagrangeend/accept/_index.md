---
title: StructuredDocumentTagRangeEnd.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Esplora il metodo Accept di StructuredDocumentTagRangeEnd. Migliora l'elaborazione dei tuoi documenti gestendo in modo efficiente le interazioni con i visitatori.
type: docs
weight: 40
url: /it/net/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd.Accept method

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
* class [StructuredDocumentTagRangeEnd](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
