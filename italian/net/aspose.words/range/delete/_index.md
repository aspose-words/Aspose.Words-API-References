---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words per .NET
description: Rimuovi in modo efficiente tutti i caratteri all'interno di un intervallo specificato utilizzando il metodo Elimina intervallo. Semplifica le tue attività di modifica del testo senza sforzo!
type: docs
weight: 70
url: /it/net/aspose.words/range/delete/
---
## Range.Delete method

Elimina tutti i caratteri dell'intervallo.

```csharp
public void Delete()
```

## Esempi

Mostra come eliminare tutti i nodi da un intervallo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere testo alla prima sezione del documento, quindi aggiungere un'altra sezione.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Rimuovi completamente la prima sezione rimuovendo tutti i nodi
// all'interno del suo intervallo, inclusa la sezione stessa.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Guarda anche

* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
