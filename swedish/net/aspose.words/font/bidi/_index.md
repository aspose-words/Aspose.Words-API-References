---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font Bidi, styr textens egenskaper från höger till vänster för förbättrad läsbarhet och användarupplevelse i din webbdesign.
type: docs
weight: 30
url: /sv/net/aspose.words/font/bidi/
---
## Font.Bidi property

Anger om innehållet i denna körning ska ha egenskaper som skrivs från höger till vänster.

```csharp
public bool Bidi { get; set; }
```

## Anmärkningar

Den här egenskapen ska inte användas med text som är starkt vänster-till-höger-skriven när den är aktiverad. Allt beteende under det villkoret är ospecificerat. Den här egenskapen ska inte användas med text som är starkt höger-till-vänster-skriven när den är avaktiverad. Allt beteende under det villkoret är ospecificerat.

När innehållet i den här körningen visas ska alla tecken behandlas som komplexa skripttecken för formateringsändamål. Detta innebär att[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) och motsvarande teckensnitt name kommer att användas vid rendering av denna körning.

När innehållet i den här körningen visas fungerar även den här egenskapen som en höger-till-vänster-åsidosättning för characters som klassificeras som "svaga typer" och "neutrala typer".

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
