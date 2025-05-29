---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Scopri la proprietà Intervallo testo per recuperare e manipolare facilmente il testo all'interno di un intervallo specificato per una migliore gestione dei contenuti.
type: docs
weight: 60
url: /it/net/aspose.words/range/text/
---
## Range.Text property

Ottiene il testo dell'intervallo.

```csharp
public string Text { get; }
```

## Osservazioni

La stringa restituita include tutti i caratteri di controllo e speciali come descritto in[`ControlChar`](../../controlchar/).

## Esempi

Mostra come ottenere il contenuto testuale di tutti i nodi compresi in un intervallo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Guarda anche

* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
