---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words för .NET
description: Hantera enkelt förgrundsfärgen för ditt penseldrag med egenskapen Stroke ForeThemeColor. Anpassa dina designer med livfulla temafärger!
type: docs
weight: 140
url: /sv/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Hämtar eller ställer in ett ThemeColor-objekt som representerar streckets förgrundsfärg.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Exempel

Visar hur man ställer in färg, nyans och skugga för temat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Se även

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
