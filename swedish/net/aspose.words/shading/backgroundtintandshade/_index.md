---
title: Shading.BackgroundTintAndShade
second_title: Aspose.Words för .NET API Referens
description: Shading fast egendom. Hämtar eller ställer in ett dubbelt värde som gör en bakgrundstema ljusare eller mörkare.
type: docs
weight: 30
url: /sv/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Hämtar eller ställer in ett dubbelt värde som gör en bakgrundstema ljusare eller mörkare.

```csharp
public double BackgroundTintAndShade { get; set; }
```

### Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (den mörkaste) till 1 (den ljusaste) för den här egenskapen. Noll (0) är neutral. Ett försök att ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar iArgumentOutOfRangeException.

Om du ställer in den här egenskapen för Shading objekt med icke-tema colors resulterar iInvalidOperationException.

### Exempel

Visar hur man ställer in förgrunds- och bakgrundsfärger för skuggning av textur.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Se även

* class [Shading](../)
* namnutrymme [Aspose.Words](../../shading/)
* hopsättning [Aspose.Words](../../../)


