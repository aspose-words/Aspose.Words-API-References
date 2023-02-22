---
title: RevisionOptions.ShowRevisionBars
second_title: Aspose.Words per .NET API Reference
description: RevisionOptions proprietà. Consente di specificare se le barre di revisione devono essere visualizzate vicino a righe contenenti contenuto rivisto. Il valore predefinito è True.
type: docs
weight: 180
url: /it/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Consente di specificare se le barre di revisione devono essere visualizzate vicino a righe contenenti contenuto rivisto. Il valore predefinito è True.

```csharp
public bool ShowRevisionBars { get; set; }
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

* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../revisionoptions/)
* assemblea [Aspose.Words](../../../)


