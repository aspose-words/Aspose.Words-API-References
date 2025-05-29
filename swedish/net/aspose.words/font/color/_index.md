---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckenfärg för att enkelt anpassa textfärger i dina designer. Förbättra läsbarhet och estetik med livfulla, iögonfallande nyanser!
type: docs
weight: 70
url: /sv/net/aspose.words/font/color/
---
## Font.Color property

Hämtar eller ställer in teckensnittets färg.

```csharp
public Color Color { get; set; }
```

## Exempel

Visar hur man infogar formaterad text med hjälp av DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsformatering och lägg sedan till text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Visar hur man infogar ett hyperlänkfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Infoga en hyperlänk och framhäv den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falskt);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + vänsterklicka på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
