---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font UnderlineColor för att enkelt anpassa teckensnittets understrykningsfärg för förbättrad textstil och visuell attraktionskraft.
type: docs
weight: 550
url: /sv/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Hämtar eller ställer in färgen på understrykningen som tillämpas på teckensnittet.

```csharp
public Color UnderlineColor { get; set; }
```

## Exempel

Visar hur man konfigurerar stil och färg för en understrykning av text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
