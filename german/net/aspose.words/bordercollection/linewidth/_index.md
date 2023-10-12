---
title: BorderCollection.LineWidth
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ruft die Rahmenbreite in Punkten ab oder legt sie fest.
type: docs
weight: 90
url: /de/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Ruft die Rahmenbreite in Punkten ab oder legt sie fest.

```csharp
public double LineWidth { get; set; }
```

### Bemerkungen

Gibt die Breite des ersten Rahmens in der Sammlung zurück.

Legt die Breite aller Rahmen in der Sammlung fest, mit Ausnahme diagonaler Ränder.

### Beispiele

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
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


