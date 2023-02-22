---
title: Section.Accept
second_title: Aspose.Words per .NET API Reference
description: Section metodo. Accetta un visitatore.
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

Vero se tutti i nodi sono stati visitati; false se DocumentVisitor ha interrotto l'operazione prima di visitare tutti i nodi.

### Osservazioni

Enumera su questo nodo e tutti i suoi figli. Ogni nodo chiama un metodo corrispondente su DocumentVisitor.

Per ulteriori informazioni, vedere il modello di progettazione del visitatore.

Chiama DocumentVisitor.VisitSectionStart, quindi chiama Accept per tutti i nodi figlio della sezione e chiama DocumentVisitor.VisitSectionEnd alla fine.

### Guarda anche

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* spazio dei nomi [Aspose.Words](../../section/)
* assemblea [Aspose.Words](../../../)


