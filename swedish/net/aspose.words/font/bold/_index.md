---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words för .NET
description: Font Bold fast egendom. Sant om teckensnittet är formaterat med fet stil i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/font/bold/
---
## Font.Bold property

Sant om teckensnittet är formaterat med fet stil.

```csharp
public bool Bold { get; set; }
```

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
