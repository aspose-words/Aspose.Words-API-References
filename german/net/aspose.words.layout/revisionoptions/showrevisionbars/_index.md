---
title: RevisionOptions.ShowRevisionBars
second_title: Aspose.Words für .NET-API-Referenz
description: RevisionOptions eigendom. Ermöglicht die Angabe ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. Der Standardwert istWAHR .
type: docs
weight: 180
url: /de/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. Der Standardwert ist`WAHR` .

```csharp
public bool ShowRevisionBars { get; set; }
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

* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../revisionoptions/)
* Montage [Aspose.Words](../../../)


