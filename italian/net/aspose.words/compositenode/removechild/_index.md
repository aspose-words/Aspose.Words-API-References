---
title: CompositeNode.RemoveChild
second_title: Aspose.Words per .NET API Reference
description: CompositeNode metodo. Rimuove il nodo figlio specificato.
type: docs
weight: 180
url: /it/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

Rimuove il nodo figlio specificato.

```csharp
public Node RemoveChild(Node oldChild)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| oldChild | Node | Il nodo da rimuovere. |

### Valore di ritorno

Il nodo rimosso.

### Osservazioni

Il genitore di oldChild viene impostato su null dopo la rimozione del nodo.

### Esempi

Mostra come utilizzare i metodi di Node e CompositeNode per rimuovere una sezione prima dell'ultima sezione nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Entrambe le sezioni sono fratelli l'uno dell'altro.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Rimuove una sezione in base alla sua relazione di pari livello con un'altra sezione.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La sezione che abbiamo rimosso è stata la prima, lasciando il documento solo con la seconda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)


