---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words för .NET
description: Skapa kraftfulla dokument utan ansträngning med DocumentBuilder. Initiera en ny instans och effektivisera din dokumenthantering idag!
type: docs
weight: 10
url: /sv/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Initierar en ny instans av den här klassen.

```csharp
public DocumentBuilder()
```

## Anmärkningar

Skapar en ny[`DocumentBuilder`](../)objekt och fäster det vid ett nytt[`Document`](../../document/) objekt.

## Exempel

Visar hur man infogar formaterad text med hjälp av DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsformatering och lägg sedan till text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Initierar en ny instans av den här klassen.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Anmärkningar

Skapar en ny[`DocumentBuilder`](../)objekt och fäster det vid ett nytt[`Document`](../../document/) object. Ytterligare alternativ för dokumentbyggande kan anges.

## Exempel

Visar hur man ignorerar tabellformatering för innehåll efteråt.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Lägger till innehåll före tabellen.
// Standardteckenstorleken är 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändrar teckenstorleken inuti tabellen.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Om ContextTableFormatting är sant, tillämpas inte tabellformatering på innehållet efteråt.
// Om ContextTableFormatting är falskt, tillämpas tabellformatering på innehållet efteråt.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Se även

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Initierar en ny instans av den här klassen.

```csharp
public DocumentBuilder(Document doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | Document | De[`Document`](../../document/) föremål att fästa vid. |

## Anmärkningar

Skapar en ny[`DocumentBuilder`](../) objekt, fäster vid det angivna[`Document`](../../document/) objekt. Markören är placerad i början av dokumentet.

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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Initierar en ny instans av den här klassen.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | Document | De[`Document`](../../document/) föremål att fästa vid. |
| options | DocumentBuilderOptions | Ytterligare alternativ för dokumentbyggprocessen. |

## Anmärkningar

Skapar en ny[`DocumentBuilder`](../) objekt, fäster vid det angivna[`Document`](../../document/) objekt. Markören är placerad i början av dokumentet.

## Exempel

Visar hur man ignorerar tabellformatering för innehåll efteråt.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Lägger till innehåll före tabellen.
// Standardteckenstorleken är 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändrar teckenstorleken inuti tabellen.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Om ContextTableFormatting är sant, tillämpas inte tabellformatering på innehållet efteråt.
// Om ContextTableFormatting är falskt, tillämpas tabellformatering på innehållet efteråt.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Se även

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
