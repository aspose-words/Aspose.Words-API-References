---
title: LayoutOptions.RevisionOptions
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutOptions eigendom. Ruft Revisionsoptionen ab.
type: docs
weight: 70
url: /de/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Ruft Revisionsoptionen ab.

```csharp
public RevisionOptions RevisionOptions { get; }
```

### Beispiele

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Revision einfügen und dann die Farbe aller Revisionen in Grün ändern.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie die Leiste, die links von jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../layoutoptions/)
* Montage [Aspose.Words](../../../)


