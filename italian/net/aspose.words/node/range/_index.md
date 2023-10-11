---
title: Node.Range
second_title: Aspose.Words per .NET API Reference
description: Node proprietà. Restituisce aRange oggetto che rappresenta la porzione di documento contenuta in questo nodo.
type: docs
weight: 80
url: /it/net/aspose.words/node/range/
---
## Node.Range property

Restituisce a[`Range`](../../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo.

```csharp
public Range Range { get; }
```

### Esempi

Mostra come eliminare tutti i nodi da un intervallo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge testo alla prima sezione del documento, quindi aggiunge un'altra sezione.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Rimuove completamente la prima sezione rimuovendo tutti i nodi
// all'interno del suo intervallo, inclusa la sezione stessa.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Guarda anche

* class [Range](../../range/)
* class [Node](../)
* spazio dei nomi [Aspose.Words](../../node/)
* assemblea [Aspose.Words](../../../)


