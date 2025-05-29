---
title: LayoutOptions.RevisionOptions
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft „LayoutOptions RevisionOptions“, um einfach auf Revisionseinstellungen zuzugreifen und diese anzupassen und so die Dokumentkontrolle und Flexibilität zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Ruft Revisionsoptionen ab.

```csharp
public RevisionOptions RevisionOptions { get; }
```

## Beispiele

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen in Grün.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie den Balken, der links neben jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
