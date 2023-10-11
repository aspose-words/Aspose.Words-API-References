---
title: StructuredDocumentTagRangeEnd.Accept
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagRangeEnd metodo. Accetta un visitatore.
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

### Osservazioni

Enumera questo nodo e tutti i relativi figli. Ogni nodo chiama un metodo corrispondente[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Per maggiori informazioni vedere il modello di progettazione Visitor.

### Guarda anche

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeEnd](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* assemblea [Aspose.Words](../../../)


