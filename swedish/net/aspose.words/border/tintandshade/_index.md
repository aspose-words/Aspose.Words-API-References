---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words för .NET
description: Upptäck Border TintAndShade, justera enkelt färgernas ljusstyrka med ett enkelt dubbelt värde för fantastiska designförbättringar. Perfekt för dina kreativa projekt!
type: docs
weight: 80
url: /sv/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en färg.

```csharp
public double TintAndShade { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Utlöses om du försöker ställa in den här egenskapen till ett värde mindre än -1 eller mer än 1. |
| InvalidOperationException | Utlöser om den här egenskapen anges för Border-objekt med icke-temafärger. |

## Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen. Noll (0) är neutralt.

## Exempel

Visar hur man infogar ett stycke med en övre kantlinje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ endast in ThemeColor när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
