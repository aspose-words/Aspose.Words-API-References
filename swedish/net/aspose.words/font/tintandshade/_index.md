---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font TintAndShade för att enkelt justera färger! Ljusa eller mörka nyanser för livfulla designer. Förbättra dina projekt utan ansträngning!
type: docs
weight: 530
url: /sv/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en färg.

```csharp
public double TintAndShade { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta om den här egenskapen sätts till ett värde mindre än -1 eller större än 1. |
| InvalidOperationException | Kasta om den här egenskapen är satt för[`Font`](../) objekt med färger som inte är temafärger. |

## Anmärkningar

De tillåtna värdena ligger i intervallet -1 (mörkast) till 1 (ljusast) för den här egenskapen.

Noll (0) är neutral.

## Exempel

Visar hur man skapar och använder temainriktad stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Skapa lite stil med temats teckensnittsegenskaper.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
