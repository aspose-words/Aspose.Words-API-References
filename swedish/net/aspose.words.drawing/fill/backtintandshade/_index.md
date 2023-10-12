---
title: Fill.BackTintAndShade
second_title: Aspose.Words för .NET API Referens
description: Fill fast egendom. Hämtar eller ställer in ett dubbelt värde som gör bakgrundsfärgen ljusare eller mörkare.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Hämtar eller ställer in ett dubbelt värde som gör bakgrundsfärgen ljusare eller mörkare.

```csharp
public double BackTintAndShade { get; set; }
```

### Anmärkningar

De tillåtna värdena ligger inom intervallet från -1 (den mörkaste) till 1 (den ljusaste) för den här egenskapen. Noll (0) är neutral. Ett försök att ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar iArgumentOutOfRangeException.

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

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)


