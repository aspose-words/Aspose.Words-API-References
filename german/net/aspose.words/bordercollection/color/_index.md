---
title: BorderCollection.Color
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ruft die Rahmenfarbe ab oder legt sie fest.
type: docs
weight: 20
url: /de/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Ruft die Rahmenfarbe ab oder legt sie fest.

```csharp
public Color Color { get; set; }
```

### Bemerkungen

Gibt die Farbe des ersten Rahmens in der Auflistung zurück.

Legt die Farbe aller Rahmen in der Sammlung mit Ausnahme diagonaler Rahmen fest.

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


