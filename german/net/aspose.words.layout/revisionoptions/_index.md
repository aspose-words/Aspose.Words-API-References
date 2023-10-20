---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.RevisionOptions klas. Ermöglicht die Steuerung wie Dokumentrevisionen während des Layoutprozesses gehandhabt werden in C#.
type: docs
weight: 3390
url: /de/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layoutprozesses gehandhabt werden.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Fixed-Page-Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class RevisionOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Kommentare verwendet werden soll. Der Standardwert istRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für gelöschte Inhalte verwendet werden sollDeletion . Der Standardwert istByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den gelöschten Inhalt angewendet werden sollDeletion . Der Standardwert istStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für eingefügte Inhalte verwendet werden sollInsertion . Der Standardwert istByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den eingefügten Inhalt angewendet werden sollInsertion . Der Standardwert istUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Der Standardwert istCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet werden soll, aus denen Inhalte verschoben wurdenMoving . Der Standardwert istByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, aus denen Inhalte verschoben wurdenMoving . Der Standardwert istDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet werden soll, in die Inhalte verschoben wurdenMoving . Der Standardwert istByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, in die Inhalte verschoben wurdenMoving . Der Standardwert istDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Inhalte bei Änderungen der Formatierungseigenschaften verwendet werden sollFormatChange Der Standardwert istNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Ermöglicht die Angabe des Effekts für Inhaltsbereiche bei Änderungen der FormatierungseigenschaftenFormatChange Der Standardwert istNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet werden soll, die Dokumentzeilen kennzeichnen, die überarbeitete Informationen enthalten. Der Standardwert istRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Ruft die Renderposition der Revisionsbalken ab oder legt sie fest. Der Standardwert istOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Ruft die Breite der Revisionsbalken und Punkte ab oder legt diese fest. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Ermöglicht die Angabe, ob die Revisionen in den Sprechblasen gerendert werden. Der Standardwert istNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. Der Standardwert ist`WAHR` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Ermöglicht die Angabe, ob Revisionstext mit einem speziellen Formatierungs-Markup markiert werden soll. Der Standardwert ist`WAHR` . |

## Beispiele

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
