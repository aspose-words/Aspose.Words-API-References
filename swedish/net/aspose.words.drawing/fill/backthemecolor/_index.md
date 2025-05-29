---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words för .NET
description: Anpassa din design med egenskapen BackThemeColor. Ställ enkelt in ett ThemeColor-objekt för att förbättra din bakgrundsfyllning och höja användarupplevelsen.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Hämtar eller ställer in ett ThemeColor-objekt som representerar bakgrundsfärgen för fyllningen.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Exempel

Visar hur man ställer in temafärg för förgrunds-/bakgrundsformfärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Obs: använd inte "BackThemeColor" och "BackTintAndShade" för typsnittsfyllning.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Se även

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
