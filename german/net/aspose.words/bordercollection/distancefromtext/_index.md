---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words für .NET
description: BorderCollection DistanceFromText eigendom. Ermittelt oder legt den Abstand des Rahmens vom Text in Punkten fest in C#.
type: docs
weight: 40
url: /de/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Ermittelt oder legt den Abstand des Rahmens vom Text in Punkten fest.

```csharp
public double DistanceFromText { get; set; }
```

## Bemerkungen

Ruft den Abstand vom Text für den ersten Rahmen ab.

Legt den Abstand vom Text für alle Rahmen in der Sammlung mit Ausnahme diagonaler Ränder fest.

Hat keine Auswirkung und wird für die Ränder von Tabellenzellen automatisch auf Null zurückgesetzt.

## Beispiele

Zeigt, wie man einen grünen, wellenförmigen Seitenrand mit einem Schatten erstellt.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Siehe auch

* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
