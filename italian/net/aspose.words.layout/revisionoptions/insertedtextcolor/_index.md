---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: Aspose.Words per .NET
description: Personalizza la tua esperienza di modifica con la proprietà InsertedTextColor di RevisionOptions, impostando colori univoci per il contenuto inserito. Impostazione predefinita ByAuthor.
type: docs
weight: 60
url: /it/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Permette di specificare il colore da utilizzare per il contenuto inseritoInsertion . Il valore predefinito èByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
