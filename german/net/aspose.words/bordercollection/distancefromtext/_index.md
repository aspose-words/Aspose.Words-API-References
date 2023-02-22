---
title: BorderCollection.DistanceFromText
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ermittelt oder setzt den Abstand des Randes vom Text in Punkten.
type: docs
weight: 40
url: /de/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Ermittelt oder setzt den Abstand des Randes vom Text in Punkten.

```csharp
public double DistanceFromText { get; set; }
```

### Bemerkungen

Ruft den Abstand vom Text für den ersten Rahmen ab.

Legt den Abstand vom Text für alle Ränder in der Sammlung außer diagonalen Rändern fest.

Hat keine Auswirkung und wird für Ränder von Tabellenzellen automatisch auf Null zurückgesetzt.

### Beispiele

Zeigt, wie Sie einen grünen wellenförmigen Seitenrand mit einem Schatten erstellen.

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
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


