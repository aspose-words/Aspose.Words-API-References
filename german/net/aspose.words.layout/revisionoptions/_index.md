---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Layout.RevisionOptions, um Dokumentrevisionen effizient zu verwalten und Ihren Layoutprozess für optimale Ergebnisse zu verbessern.
type: docs
weight: 3840
url: /de/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Ermöglicht die Steuerung der Handhabung von Dokumentrevisionen während des Layoutprozesses.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Festseitenformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class RevisionOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Ermöglicht die Angabe der Farbe für Kommentare. Der Standardwert istRed . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für gelöschte Zellen verwendet werden sollDeletion . Der Standardwert istPink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für gelöschte Inhalte verwendet werden sollDeletion . Der Standardwert istByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den gelöschten Inhalt angewendet werden sollDeletion . Der Standardwert istStrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für eingefügte Zellen verwendet werden sollInsertion . Der Standardwert istBlue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für eingefügte Inhalte verwendet werden sollInsertion . Der Standardwert istByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den eingefügten Inhalt angewendet werden sollInsertion . Der Standardwert istUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Der Standardwert istCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe für Bereiche, aus denen Inhalte verschoben wurdenMoving . Der Standardwert istByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, aus denen Inhalte verschoben wurdenMoving . Der Standardwert istDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe für Bereiche, in die Inhalte verschoben wurdenMoving . Der Standardwert istByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, in die Inhalte verschoben wurdenMoving . Der Standardwert istDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Inhalte mit Änderungen der Formatierungseigenschaften verwendet werden sollFormatChange Der Standardwert istNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Ermöglicht die Festlegung der Auswirkung auf Inhaltsbereiche bei Änderungen der FormatierungseigenschaftenFormatChange Der Standardwert istNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Ermöglicht die Angabe der Farbe für Seitenleisten, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert istRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Ruft die Rendering-Position der Revisionsbalken ab oder legt sie fest. Der Standardwert istOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Ruft die Breite der Revisionsbalken (Punkte) ab oder legt sie fest. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Ermöglicht die Angabe, ob die Revisionen in den Sprechblasen dargestellt werden. Der Standardwert istNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten Textes angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt angezeigt werden sollen. Der Standardwert ist`WAHR` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Ermöglicht die Angabe, ob Revisionstext mit speziellen Formatierungsmarkierungen gekennzeichnet werden soll. Der Standardwert ist`WAHR` . |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
