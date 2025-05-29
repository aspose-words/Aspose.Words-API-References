---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckensnittskontur. Formatera enkelt teckensnitt som konturer för en unik designkänsla. Förbättra din typografi med den här enkla funktionen!
type: docs
weight: 300
url: /sv/net/aspose.words/font/outline/
---
## Font.Outline property

Sant om teckensnittet är formaterat som kontur.

```csharp
public bool Outline { get; set; }
```

## Exempel

Visar hur man skapar en textsekvens formaterad som disposition.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in flaggan Kontur för att ändra textens fyllningsfärg till vit och
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
