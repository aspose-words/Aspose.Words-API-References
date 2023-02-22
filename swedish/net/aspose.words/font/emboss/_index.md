---
title: Font.Emboss
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. True om teckensnittet är formaterat som relief.
type: docs
weight: 100
url: /sv/net/aspose.words/font/emboss/
---
## Font.Emboss property

True om teckensnittet är formaterat som relief.

```csharp
public bool Emboss { get; set; }
```

### Exempel

Visar hur man applicerar gravyr-/präglingseffekter på text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Nedan finns två sätt att använda skuggor för att applicera en 3D-liknande effekt på texten.
// 1 - Gravera text så att det ser ut som om bokstäverna är nedsänkta på sidan:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Relief text så att det ser ut som om bokstäverna dyker upp från sidan:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


