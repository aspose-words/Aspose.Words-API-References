---
title: ParagraphFormat.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat StyleIdentifier för att enkelt hantera och anpassa styckeformat, vilket förbättrar dokumentets formatering och läsbarhet.
type: docs
weight: 360
url: /sv/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Hämtar eller ställer in den språkoberoende formateringsidentifieraren för styckeformatet som tillämpas på denna formatering.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Exempel

Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med hjälp av rubrikformat som poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen för att hämta stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster som hyperlänkar som tar oss
// till rubrikens plats när man vänsterklickar i Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fyll innehållsförteckningen genom att lägga till stycken med rubrikformat.
// Varje sådan rubrik med en nivå mellan 1 och 3 skapar en post i tabellen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// En innehållsförteckning är ett fält av en typ som behöver uppdateras för att visa ett aktuellt resultat.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Se även

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
