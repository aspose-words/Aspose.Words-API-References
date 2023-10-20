---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words för .NET
description: Border TintAndShade fast egendom. Hämtar eller ställer in ett dubbelt värde som gör en färg ljusare eller mörkare i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Hämtar eller ställer in ett dubbelt värde som gör en färg ljusare eller mörkare.

```csharp
public double TintAndShade { get; set; }
```

## Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (den mörkaste) till 1 (den ljusaste) för den här egenskapen. Noll (0) är neutral. Ett försök att ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1 resulterar iArgumentOutOfRangeException.

Att ställa in den här egenskapen för Border-objekt med icke-tema colors resulterar iInvalidOperationException.

## Exempel

Visar hur man infogar ett stycke med en övre kant.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ in ThemeColor endast när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
