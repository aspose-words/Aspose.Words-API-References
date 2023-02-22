---
title: Font.Bold
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Sant om teckensnittet är formaterat med fet stil.
type: docs
weight: 40
url: /sv/net/aspose.words/font/bold/
---
## Font.Bold property

Sant om teckensnittet är formaterat med fet stil.

```csharp
public bool Bold { get; set; }
```

### Exempel

Visar hur man infogar formaterad text med DocumentBuilder.

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
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


