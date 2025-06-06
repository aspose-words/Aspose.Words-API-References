---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „ForeThemeColor“ festlegen, um Ihr Design mit lebendigen Füllfarben anzupassen. Verbessern Sie mühelos die visuelle Attraktivität Ihres Projekts!
type: docs
weight: 80
url: /de/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Beispiele

Zeigt, wie die Designfarbe für die Vordergrund-/Hintergrundformfarbe festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Hinweis: Verwenden Sie „BackThemeColor“ und „BackTintAndShade“ nicht zum Füllen der Schriftart.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Siehe auch

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
