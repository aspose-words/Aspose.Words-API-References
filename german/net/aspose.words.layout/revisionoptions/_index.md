---
title: Class RevisionOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Layout.RevisionOptions klas. Ermöglicht die Steuerung wie Dokumentrevisionen während des Layoutprozesses gehandhabt werden.
type: docs
weight: 3190
url: /de/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layoutprozesses gehandhabt werden.

```csharp
public class RevisionOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Ermöglicht die Festlegung der für Kommentare zu verwendenden Farbe. Standardwert istRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für gelöschte Inhalte verwendet werden sollDeletion . Standardwert istByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den gelöschten Inhalt angewendet werden sollDeletion . Standardwert istStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für eingefügte Inhalte verwendet werden sollInsertion . Standardwert istByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf den eingefügten Inhalt angewendet werden sollInsertion . Standardwert istUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Standardwert istCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet werden soll, aus denen Inhalte verschoben wurdenMoving . Standardwert istByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, aus denen Inhalte verschoben wurdenMoving . Standardwert istDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Bereiche verwendet werden soll, in die Inhalte verschoben wurdenMoving . Standardwert istByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, in die Inhalte verschoben wurdenMoving . Standardwert istDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Inhalte mit Änderungen der Formatierungseigenschaften verwendet werden sollFormatChange Standardwert istNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Ermöglicht das Festlegen des Effekts für Inhaltsbereiche mit Änderungen der FormatierungseigenschaftenFormatChange Standardwert istNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet werden soll, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert istRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Ruft die Wiedergabeposition von Revisionsbalken ab oder legt sie fest. Der Standardwert istOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Holt oder setzt die Breite von Revisionsbalken, Punkten. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Ermöglicht die Angabe, ob die Revisionen in den Sprechblasen gerendert werden. Der Standardwert istNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Ermöglicht die Angabe, ob der Originaltext statt des überarbeiteten angezeigt werden soll. Der Standardwert ist False. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Ermöglicht die Angabe, ob Überarbeitungsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. Der Standardwert ist True. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Geben Sie an, ob Überarbeitungstext mit einem speziellen Formatierungs-Markup gekennzeichnet werden soll. Der Standardwert ist True. |

### Beispiele

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Revision einfügen, dann die Farbe aller Revisionen auf Grün ändern.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie den Balken, der links von jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)


