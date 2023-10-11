---
title: Fill.ForeThemeColor
second_title: Aspose.Words för .NET API Referens
description: Fill fast egendom. Hämtar eller ställer in ett ThemeColorobjekt som representerar förgrundsfärgen för fyllningen.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Hämtar eller ställer in ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

### Exempel

Visar hur du ställer in temafärg för förgrunds-/bakgrundsformfärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Obs: använd inte "BackThemeColor" och "BackTintAndShade" för teckensnittsfyllning.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Se även

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)


