---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder MoveToSection-metoden för att enkelt navigera till början av valfritt avsnitts brödtext, vilket förbättrar din dokumentredigeringseffektivitet.
type: docs
weight: 610
url: /sv/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Flyttar markören till början av texten i ett angivet avsnitt.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sectionIndex | Int32 | Indexet för det avsnitt som ska flyttas till. |

## Anmärkningar

När*sectionIndex*är större än eller lika med 0, anger den ett index från början av dokumentet där 0 är det första avsnittet. När*sectionIndex* är mindre än 0, specificerade det ett index från slutet av dokumentet där -1 är det sista avsnittet.

Markören flyttas till det första stycket i[`Body`](../../body/) av det angivna avsnittet.

## Exempel

Visar hur man skapar sidhuvuden och sidfot i ett dokument med hjälp av DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange att vi vill ha olika sidhuvuden och sidfot för första, jämna och udda sidor.
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

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
