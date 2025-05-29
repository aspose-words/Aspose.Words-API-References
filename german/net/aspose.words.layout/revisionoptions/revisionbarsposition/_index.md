---
title: RevisionOptions.RevisionBarsPosition
linktitle: RevisionBarsPosition
articleTitle: RevisionBarsPosition
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie die Eigenschaft „RevisionBarsPosition“ in „RevisionOptions“ anpassen, um das Erscheinungsbild Ihres Dokuments zu verbessern. Die Standardeinstellung ist „Außen“.
type: docs
weight: 160
url: /de/net/aspose.words.layout/revisionoptions/revisionbarsposition/
---
## RevisionOptions.RevisionBarsPosition property

Ruft die Rendering-Position der Revisionsbalken ab oder legt sie fest. Der Standardwert istOutside .

```csharp
public HorizontalAlignment RevisionBarsPosition { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Werte vonCenter UndInside sind nicht zulässig. |

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

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
