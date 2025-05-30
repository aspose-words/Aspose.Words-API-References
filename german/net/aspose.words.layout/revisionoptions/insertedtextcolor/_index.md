---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: Aspose.Words für .NET
description: Passen Sie Ihr Bearbeitungserlebnis mit der RevisionOptions InsertedTextColor-Eigenschaft an und legen Sie eindeutige Farben für eingefügte Inhalte fest. Standard ByAuthor.
type: docs
weight: 60
url: /de/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Ermöglicht die Angabe der Farbe, die für eingefügte Inhalte verwendet werden sollInsertion . Der Standardwert istByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
