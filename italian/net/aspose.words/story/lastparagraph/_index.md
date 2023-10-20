---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words per .NET
description: Story LastParagraph proprietà. Ottiene lultimo paragrafo della storia in C#.
type: docs
weight: 20
url: /it/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Ottiene l'ultimo paragrafo della storia.

```csharp
public Paragraph LastParagraph { get; }
```

## Esempi

Mostra come spostare la posizione del cursore di DocumentBuilder su un nodo specificato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Il generatore di documenti ha un cursore, che funge da parte del documento
// dove il builder aggiunge nuovi nodi quando utilizziamo i suoi metodi di costruzione del documento.
// Questo cursore funziona allo stesso modo del cursore lampeggiante di Microsoft Word,
// e finisce sempre immediatamente dopo qualsiasi nodo appena inserito dal builder.
// Per aggiungere contenuto a una parte diversa del documento,
// possiamo spostare il cursore su un nodo diverso con il metodo "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Il cursore è ora davanti al nodo su cui lo abbiamo spostato.
// L'aggiunta di una seconda esecuzione la inserirà davanti alla prima esecuzione.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Sposta il cursore alla fine del documento per continuare ad aggiungere testo alla fine come prima.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Guarda anche

* class [Paragraph](../../paragraph/)
* class [Story](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
