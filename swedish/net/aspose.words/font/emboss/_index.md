---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words för .NET
description: Upptäck funktionen Font Emboss, som förbättrar din text med en snygg präglad effekt för iögonfallande design. Förbättra din typografi idag!
type: docs
weight: 100
url: /sv/net/aspose.words/font/emboss/
---
## Font.Emboss property

Sant om teckensnittet är formaterat som präglat.

```csharp
public bool Emboss { get; set; }
```

## Exempel

Visar hur man applicerar gravyr-/präglingseffekter på text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Nedan följer två sätt att använda skuggor för att applicera en 3D-liknande effekt på texten.
// 1 - Gravera text så att det ser ut som att bokstäverna är nedsänkta i sidan:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Reliefmarkera texten så att det ser ut som att bokstäverna sticker ut från sidan:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
