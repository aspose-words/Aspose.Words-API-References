---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words für .NET
description: Verwalten Sie die Vordergrundfarbe Ihres Strichs mühelos mit der Stroke ForeThemeColor-Eigenschaft. Passen Sie Ihre Designs mit lebendigen Themenfarben an!
type: docs
weight: 140
url: /de/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Vordergrundfarbe des Strichs darstellt.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Beispiele

Zeigt, wie man Farbe, Farbton und Schattierung für das Design einstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Siehe auch

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
