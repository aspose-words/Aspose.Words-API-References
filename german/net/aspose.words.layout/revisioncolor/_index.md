---
title: Enum RevisionColor
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Layout.RevisionColor opsomming. Ermöglicht die Angabe der Farbe von Dokumentrevisionen.
type: docs
weight: 3380
url: /de/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Ermöglicht die Angabe der Farbe von Dokumentrevisionen.

```csharp
public enum RevisionColor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `0` | Standard. |
| Black | `1` | Stellt 000000 Farben dar. |
| Blue | `2` | Stellt die Farbe 2e97d3 dar. |
| BrightGreen | `3` | Stellt die Farbe 84a35b dar. |
| ClassicBlue | `4` | Stellt die Farbe 0000ff dar. |
| ClassicRed | `5` | Stellt die Farbe ff0000 dar. |
| DarkBlue | `6` | Stellt die Farbe 376e96 dar. |
| DarkRed | `7` | Stellt 881824 Farben dar. |
| DarkYellow | `8` | Stellt die Farbe e09a2b dar. |
| Gray25 | `9` | Stellt die Farbe a0a3a9 dar. |
| Gray50 | `10` | Stellt die Farbe 50565e dar. |
| Green | `11` | Stellt die Farbe 2c6234 dar. |
| Pink | `12` | Stellt die Farbe ce338f dar. |
| Red | `13` | Stellt die Farbe b5082e dar. |
| Teal | `14` | Stellt die Farbe 1b9cab dar. |
| Turquoise | `15` | Stellt die Farbe 3eafc2 dar. |
| Violet | `16` | Stellt 633277 Farben dar. |
| White | `17` | Stellt die ffffff-Farbe dar. |
| Yellow | `18` | Stellt die Farbe fad272 dar. |
| NoHighlight | `19` | Es wird keine Farbe verwendet, um Revisionsänderungen hervorzuheben. |
| ByAuthor | `20` | Überarbeitungen jedes Autors erhalten eine eigene Farbe zur Hervorhebung aus einem vordefinierten Satz kontrastreicher Farben. |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)


