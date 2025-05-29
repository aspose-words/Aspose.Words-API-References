---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup PageNumberStyle för att enkelt anpassa sidnummerformatet för förbättrad dokumentpresentation och tydlighet.
type: docs
weight: 320
url: /sv/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Hämtar eller ställer in sidnummerformatet.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## Exempel

Visar hur man ställer in sidnumrering i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Flytta dokumentbyggaren till den första sektionens primära rubrik,
// som varje sida i det avsnittet kommer att visa.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Infoga ett PAGE-fält, som visar numret på den aktuella sidan.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurera sektionen så att sidantalet som PAGE-fälten visar börjar från 5.
// Konfigurera också alla PAGE-fält så att deras sidnummer visas med versaler i romerska siffror.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Skapa ytterligare en primär rubrik för den andra sektionen, med ytterligare ett PAGE-fält.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurera sektionen så att sidantalet som PAGE-fälten visar börjar från 10.
// Konfigurera också alla PAGE-fält så att deras sidnummer visas med arabiska siffror.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Se även

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
