---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words für .NET
description: Fill BackTintAndShade eigendom. Ruft einen DoubleWert ab oder legt diesen fest der die Hintergrundfarbe heller oder dunkler macht in C#.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Ruft einen Double-Wert ab oder legt diesen fest, der die Hintergrundfarbe heller oder dunkler macht.

```csharp
public double BackTintAndShade { get; set; }
```

## Bemerkungen

Die zulässigen Werte liegen für diese Eigenschaft im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder mehr als 1 festzulegen, führt zuArgumentOutOfRangeException.

## Beispiele

Zeigt, wie die Designfarbe für die Vordergrund-/Hintergrundformfarbe festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Hinweis: Verwenden Sie nicht „BackThemeColor“ und „BackTintAndShade“ für die Schriftartfüllung.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
