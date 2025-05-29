---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words för .NET
description: Justera egenskapen Stroke ForeTintAndShade för att enkelt ljusa eller mörka upp linjens förgrundsfärg och förbättra den visuella effekten.
type: docs
weight: 150
url: /sv/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp linjens förgrundsfärg.

```csharp
public double ForeTintAndShade { get; set; }
```

## Anmärkningar

De tillåtna värdena ligger inom intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen. Noll (0) är neutralt. Om du försöker ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar det iArgumentOutOfRangeException.

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

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
