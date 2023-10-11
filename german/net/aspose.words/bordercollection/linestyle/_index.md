---
title: BorderCollection.LineStyle
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ruft den Rahmenstil ab oder legt ihn fest.
type: docs
weight: 80
url: /de/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Ruft den Rahmenstil ab oder legt ihn fest.

```csharp
public LineStyle LineStyle { get; set; }
```

### Bemerkungen

Gibt den Stil des ersten Rahmens in der Sammlung zurück.

Legt den Stil aller Rahmen in der Sammlung fest, mit Ausnahme diagonaler Ränder.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


