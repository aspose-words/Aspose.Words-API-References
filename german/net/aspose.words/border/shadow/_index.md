---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words für .NET
description: Border Shadow eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob der Rahmen einen Schatten hat in C#.
type: docs
weight: 60
url: /de/net/aspose.words/border/shadow/
---
## Border.Shadow property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob der Rahmen einen Schatten hat.

```csharp
public bool Shadow { get; set; }
```

## Bemerkungen

Damit in Microsoft Word ein Rahmen einen Schatten hat, müssen die Ränder auf allen vier Seiten (links, oben, rechts und unten) den gleichen Typ, die gleiche Breite und die gleiche Farbe haben und die Eigenschaft „Schatten“ muss auf alle gesetzt sein`WAHR`.

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

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
