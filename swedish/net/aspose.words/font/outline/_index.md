---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words för .NET
description: Font Outline fast egendom. Sant om teckensnittet är formaterat som kontur i C#.
type: docs
weight: 290
url: /sv/net/aspose.words/font/outline/
---
## Font.Outline property

Sant om teckensnittet är formaterat som kontur.

```csharp
public bool Outline { get; set; }
```

## Exempel

Visar hur man skapar en serie text formaterad som disposition.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in Outline-flaggan för att ändra textens fyllnadsfärg till vit och
 // lämna en tunn kontur runt varje tecken i textens ursprungliga färg.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
