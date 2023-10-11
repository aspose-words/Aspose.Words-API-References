---
title: Node.PreviousSibling
second_title: Aspose.Words per .NET API Reference
description: Node proprietà. Ottiene il nodo immediatamente precedente questo nodo.
type: docs
weight: 70
url: /it/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Ottiene il nodo immediatamente precedente questo nodo.

```csharp
public Node PreviousSibling { get; }
```

### Osservazioni

Se non è presente alcun nodo precedente, a`nullo` viene restituito.

### Esempi

Mostra come utilizzare i metodi Node e CompositeNode per rimuovere una sezione prima dell'ultima sezione nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Entrambe le sezioni sono sorelle l'una dell'altra.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Rimuove una sezione in base alla sua relazione di pari livello con un'altra sezione.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// La sezione che abbiamo rimosso era la prima, lasciando nel documento solo la seconda.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Guarda anche

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../node/)
* assemblea [Aspose.Words](../../../)


