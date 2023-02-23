---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words for .NET API Reference
description: PageSetup property. True if the document has different headers and footers for oddnumbered and evennumbered pages in C#.
type: docs
weight: 280
url: /net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

True if the document has different headers and footers for odd-numbered and even-numbered pages.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Remarks

Note, changing this property affects all sections in the document.

## Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
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

Shows how to enable or disable even page headers/footers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two types of header/footers.
// 1 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer. 
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 -  The "Even" header/footer, which appears on every even page of this section.
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

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "OddAndEvenPagesHeaderFooter" property to "true"
// to display the even page header/footer on even pages.
// Set the "OddAndEvenPagesHeaderFooter" property to "false"
// to display the primary header/footer on even pages.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
