---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words für .NET
description: Fill BackThemeColor eigendom. Ruft ein ThemeColorObjekt ab oder legt dieses fest das die Hintergrundfarbe für die Füllung darstellt in C#.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Ruft ein ThemeColor-Objekt ab oder legt dieses fest, das die Hintergrundfarbe für die Füllung darstellt.

```csharp
public ThemeColor BackThemeColor { get; set; }
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

// Hinweis: Verwenden Sie nicht „BackThemeColor“ und „BackTintAndShade“ für die Schriftartfüllung.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Siehe auch

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
