---
title: LayoutOptions.RevisionOptions
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words per .NET
description: Esplora la proprietà LayoutOptions RevisionOptions per accedere facilmente alle impostazioni di revisione e personalizzarle, per un maggiore controllo e flessibilità dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Ottiene le opzioni di revisione.

```csharp
public RevisionOptions RevisionOptions { get; }
```

## Esempi

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga rivista.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
