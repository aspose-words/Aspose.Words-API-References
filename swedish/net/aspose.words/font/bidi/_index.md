---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words för .NET
description: Font Bidi fast egendom. Anger om innehållet i denna körning ska ha högertillvänsteregenskaper i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/font/bidi/
---
## Font.Bidi property

Anger om innehållet i denna körning ska ha höger-till-vänster-egenskaper.

```csharp
public bool Bidi { get; set; }
```

## Anmärkningar

Den här egenskapen, när den är på, ska inte användas med starkt vänster-till-höger-text. Allt beteende under det villkoret är ospecificerat. Den här egenskapen, när den är avstängd, ska inte användas med stark text från höger till vänster. Allt beteende under det villkoret är ospecificerat.

När innehållet i denna körning visas ska alla tecken behandlas som komplexa skripttecken för formatting ändamål. Detta innebär att[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) och ett motsvarande teckensnitt name kommer att användas när den här körningen renderas.

När innehållet i denna körning visas fungerar den här egenskapen som en åsidosättning från höger till vänster för characters som klassificeras som "svaga typer" och "neutrala typer".

## Exempel

Visar hur man definierar separata uppsättningar teckensnittsinställningar för text från höger till vänster och höger till vänster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definiera en uppsättning teckensnittsinställningar för text från vänster till höger.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definiera ytterligare en uppsättning teckensnittsinställningar för text från höger till vänster.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Vi kan använda Bidi-flaggan för att indikera om texten vi ska lägga till
// med dokumentbyggaren är från höger till vänster. När vi lägger till text med denna flagga inställd på sant,
// det kommer att formateras med hjälp av teckensnittsinställningarna från höger till vänster.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Ställ in flaggan på false och lägg sedan till vänster till höger text.
// Dokumentbyggaren formaterar dessa med hjälp av teckensnittsinställningarna från vänster till höger.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
