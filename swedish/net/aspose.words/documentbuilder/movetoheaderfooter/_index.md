---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words för .NET
description: Navigera enkelt till sidhuvuden och sidfot med DocumentBuilder MoveToHeaderFooter-metoden, vilket förbättrar din dokumentredigeringseffektivitet.
type: docs
weight: 580
url: /sv/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Flyttar markören till början av ett sidhuvud eller en sidfot i det aktuella avsnittet.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Anger vilket sidhuvud eller sidfot som ska flyttas till. |

## Anmärkningar

När du har flyttat markören till ett sidhuvud eller en sidfot kan du använda resten av[`DocumentBuilder`](../) metoder för att ändra innehållet i sidhuvudet eller sidfoten.

Om du vill skapa olika sidhuvuden och sidfot för första sidan behöver du för att ställa in[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Om du vill skapa olika sidhuvuden och sidfot för jämna och udda sidor behöver du för att ställa in[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Använda[`MoveToSection`](../movetosection/) för att flytta ut ur rubriken till huvudtexten.

## Exempel

Visar hur man infogar en bild och använder den som vattenstämpel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga bilden i sidhuvudet så att den syns på varje sida.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Placera bilden i mitten av sidan.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

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

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
