---
title: Section.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Section Accept metodo. Accetta un visitatore in C#.
type: docs
weight: 70
url: /it/net/aspose.words/section/accept/
---
## Section.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà i nodi. |

### Valore di ritorno

Vero se tutti i nodi sono stati visitati; falso se[`DocumentVisitor`](../../documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.

## Osservazioni

Enumera questo nodo e tutti i relativi figli. Ogni nodo chiama un metodo corrispondente[`DocumentVisitor`](../../documentvisitor/).

Per maggiori informazioni vedere il modello di progettazione Visitor.

Chiamate[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , poi chiama[`Accept`](../../node/accept/) per tutti i nodi figlio della sezione e chiamate[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) alla fine.

### Guarda anche

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
