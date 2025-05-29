---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words för .NET
description: Upptäck funktionen Font Engrave. Formatera enkelt teckensnitt för ett elegant graverat utseende, vilket förbättrar din designs sofistikering och attraktionskraft.
type: docs
weight: 120
url: /sv/net/aspose.words/font/engrave/
---
## Font.Engrave property

Sant om teckensnittet är formaterat som graverat.

```csharp
public bool Engrave { get; set; }
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
