---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Fetstil för att enkelt identifiera om din text är fetstilad, vilket förbättrar läsbarheten och stilen för dina webbdesignprojekt.
type: docs
weight: 40
url: /sv/net/aspose.words/font/bold/
---
## Font.Bold property

Sant om teckensnittet är formaterat som fetstil.

```csharp
public bool Bold { get; set; }
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

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
