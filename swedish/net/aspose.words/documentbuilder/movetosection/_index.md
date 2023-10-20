---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words för .NET
description: DocumentBuilder MoveToSection metod. Flyttar markören till början av brödtexten i ett angivet avsnitt i C#.
type: docs
weight: 570
url: /sv/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Flyttar markören till början av brödtexten i ett angivet avsnitt.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sectionIndex | Int32 | Indexet för avsnittet att flytta till. |

## Anmärkningar

När*sectionIndex* är större än eller lika med 0, anger det ett index från början av dokumentet med 0 som den första delen. När*sectionIndex* är mindre än 0, det specificerade ett index från slutet av dokumentet med -1 som den sista sektionen.

Markören flyttas till första stycket i[`Body`](../../body/) av det angivna avsnittet.

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

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
