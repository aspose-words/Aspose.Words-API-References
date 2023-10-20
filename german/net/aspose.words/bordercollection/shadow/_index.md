---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words für .NET
description: BorderCollection Shadow eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob der Rahmen einen Schatten hat in C#.
type: docs
weight: 110
url: /de/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob der Rahmen einen Schatten hat.

```csharp
public bool Shadow { get; set; }
```

## Bemerkungen

Ruft den Wert vom ersten Rahmen in der Auflistung ab.

Legt den Wert für alle Rahmen in der Sammlung fest, mit Ausnahme diagonaler Ränder.

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
