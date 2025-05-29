---
title: Font.SizeBi
linktitle: SizeBi
articleTitle: SizeBi
second_title: Aspose.Words för .NET
description: Justera teckenstorleken i punkter för dokument som skrivs från höger till vänster utan problem. Förbättra läsbarheten och designen med vår lättanvända egenskap Font SizeBi!
type: docs
weight: 360
url: /sv/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Hämtar eller ställer in teckenstorleken i punkter som används i ett dokument som skrivs från höger till vänster.

```csharp
public double SizeBi { get; set; }
```

## Exempel

Visar hur man definierar separata uppsättningar teckensnittsinställningar för text som skrivs från höger till vänster och från höger till vänster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definiera en uppsättning teckensnittsinställningar för text från vänster till höger.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definiera en annan uppsättning teckensnittsinställningar för text från höger till vänster.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Vi kan använda Bidi-flaggan för att indikera om texten vi ska lägga till
// med dokumentbyggaren är höger-till-vänster. När vi lägger till text med denna flagga inställd på sant,
// den kommer att formateras med hjälp av teckensnittsinställningarna från höger till vänster.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Sätt flaggan till falsk och lägg sedan till text från vänster till höger.
// Dokumentbyggaren formaterar dessa med hjälp av teckensnittsinställningarna som går från vänster till höger.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
