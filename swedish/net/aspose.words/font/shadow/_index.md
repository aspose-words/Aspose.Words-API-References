---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckensnittsskugga och förbättra din text med snygga skuggeffekter för en slående visuell intrycksfullhet i dina designer.
type: docs
weight: 340
url: /sv/net/aspose.words/font/shadow/
---
## Font.Shadow property

Sant om teckensnittet är formaterat som skuggat.

```csharp
public bool Shadow { get; set; }
```

## Exempel

Visar hur man skapar en textsekvens formaterad med en skugga.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in skuggflaggan för att tillämpa en förskjuten skuggeffekt,
// får det att se ut som att bokstäverna svävar ovanför sidan.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
