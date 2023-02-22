---
title: Enum HeaderFooterType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.HeaderFooterType uppräkning. Identifierar typen av sidhuvud eller sidfot som finns i en Wordfil.
type: docs
weight: 2940
url: /sv/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Identifierar typen av sidhuvud eller sidfot som finns i en Word-fil.

```csharp
public enum HeaderFooterType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| HeaderEven | `0` | Rubrik för jämna sidor. |
| HeaderPrimary | `1` | Primär rubrik, används även för udda sidor. |
| FooterEven | `2` | Sidfot för jämna sidor. |
| FooterPrimary | `3` | Primär sidfot, används även för udda sidor. |
| HeaderFirst | `4` | Rubrik för den första sidan i avsnittet. |
| FooterFirst | `5` | Sidfot för den första sidan i avsnittet. |

### Exempel

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


