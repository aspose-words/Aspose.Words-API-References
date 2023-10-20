---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words för .NET
description: PageSetup OddAndEvenPagesHeaderFooter fast egendom. Sant om dokumentet har olika sidhuvuden och sidfötter för udda och jämna sidor i C#.
type: docs
weight: 280
url: /sv/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Sant om dokumentet har olika sidhuvuden och sidfötter för udda och jämna sidor.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Anmärkningar

Obs, att ändra den här egenskapen påverkar alla avsnitt i dokumentet.

## Exempel

Visar hur du skapar sidhuvuden och sidfötter i ett dokument med DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange att vi vill ha olika sidhuvuden och sidfötter för första, jämna och udda sidor.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Skapa rubrikerna och lägg sedan till tre sidor i dokumentet för att visa varje rubriktyp.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Visar hur du aktiverar eller inaktiverar sidhuvuden/sidfötter på jämna sidor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två typer av sidhuvud/sidfötter.
// 1 - Den "Primära" sidhuvudet/sidfoten, som visas på varje sida i avsnittet.
 // Vi kan åsidosätta den primära sidhuvudet/sidfoten med en första och en jämn sidhuvud/sidfot.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - "Jämn" sidhuvudet/sidfoten, som visas på alla jämna sidor i det här avsnittet.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Varje sektion har ett "PageSetup"-objekt som specificerar sidutseenderelaterade egenskaper
// såsom orientering, storlek och kanter.
// Ställ in egenskapen "OddAndEvenPagesHeaderFooter" till "true"
// för att visa sidhuvudet/sidfoten på jämna sidor på jämna sidor.
// Ställ in egenskapen "OddAndEvenPagesHeaderFooter" till "false"
// för att visa den primära sidhuvudet/sidfoten på jämna sidor.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
