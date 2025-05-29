---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Layout.RevisionColor, um die Farben der Dokumentrevision anzupassen, die Übersichtlichkeit zu verbessern und die Zusammenarbeit an Ihren Dokumenten zu verbessern.
type: docs
weight: 3830
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
| Black | `1` | Steht für 000000 Farben. |
| Blue | `2` | Stellt die Farbe 2e97d3 dar. |
| BrightGreen | `3` | Stellt die Farbe 84a35b dar. |
| ClassicBlue | `4` | Stellt die Farbe 0000ff dar. |
| ClassicRed | `5` | Stellt die Farbe ff0000 dar. |
| DarkBlue | `6` | Stellt die Farbe 376e96 dar. |
| DarkRed | `7` | Repräsentiert 881824 Farben. |
| DarkYellow | `8` | Stellt die Farbe e09a2b dar. |
| Gray25 | `9` | Stellt die Farbe a0a3a9 dar. |
| Gray50 | `10` | Steht für die Farbe 50565e. |
| Green | `11` | Stellt die Farbe 2c6234 dar. |
| Pink | `12` | Stellt die Farbe ce338f dar. |
| Red | `13` | Stellt die Farbe b5082e dar. |
| Teal | `14` | Stellt die Farbe 1b9cab dar. |
| Turquoise | `15` | Stellt die Farbe 3eafc2 dar. |
| Violet | `16` | Repräsentiert 633277 Farben. |
| White | `17` | Stellt die Farbe ffffff dar. |
| Yellow | `18` | Stellt die Farbe fad272 dar. |
| LightPink | `19` | Stellt die Farbe fce6f4 dar. |
| LightBlue | `20` | Stellt die Farbe e1f2fa dar. |
| LightYellow | `21` | Stellt die Fef4de-Farbe dar. |
| LightPurple | `22` | Stellt die eadfef-Farbe dar. |
| LightOrange | `23` | Stellt die Farbe fce3d0 dar. |
| LightGreen | `24` | Stellt die e9f8ce-Farbe dar. |
| Gray | `25` | Stellt eine efedierte Farbe dar. |
| NoHighlight | `26` | Es wird keine Farbe verwendet, um Revisionsänderungen hervorzuheben. |
| ByAuthor | `27` | Revisionen jedes Autors erhalten ihre eigene Farbe zur Hervorhebung aus einem vordefinierten Satz kontrastreicher Farben. |

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
