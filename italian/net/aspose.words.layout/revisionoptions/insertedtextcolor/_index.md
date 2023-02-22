---
title: RevisionOptions.InsertedTextColor
second_title: Aspose.Words per .NET API Reference
description: RevisionOptions proprietà. Consente di specificare il colore da utilizzare per il contenuto inseritoInsertion . Il valore predefinito èByAuthor .
type: docs
weight: 40
url: /it/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Consente di specificare il colore da utilizzare per il contenuto inseritoInsertion . Il valore predefinito èByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
```

### Esempi

Mostra come modificare l'aspetto delle revisioni in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuove la barra che appare a sinistra di ogni riga modificata.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../revisionoptions/)
* assemblea [Aspose.Words](../../../)


