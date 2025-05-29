---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words für .NET
description: Passen Sie Ihr Design mit der Eigenschaft „BackThemeColor“ an. Legen Sie einfach ein ThemeColor-Objekt fest, um Ihre Hintergrundfüllung zu verbessern und das Benutzererlebnis zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Hintergrundfarbe für die Füllung darstellt.

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
