---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger den maximala nivån för rubriker som fylls i navigationskartan vid export till IDPF EPUBformat. Standardvärdet är3 .
type: docs
weight: 110
url: /sv/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

Anger den maximala nivån för rubriker som fylls i navigationskartan vid export till IDPF EPUB-format. Standardvärdet är`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Anmärkningar

Navigationskarta i IDPF EPUB-format tillåter användaragenter att tillhandahålla ett enkelt sätt att navigera genom dokumentstrukturen. Vanligtvis motsvarar navigeringspunkterna rubriker i dokumentet. För att fylla i rubriker upp till nivå **N** tilldela detta värde till`EpubNavigationMapLevel`.

Som standard är tre nivåer av rubriker ifyllda: stycken med stilar **Rubrik 1** , **Rubrik 2** och **Rubrik 3**. Du kan ställa in den här egenskapen till ett värde från 1 till 9 för att begära motsvarande maxnivå. Om du ställer in den på noll kommer navigeringskartan att reduceras till att endast dokumentrot eller rötter för dokumentdelar.

### Exempel

Visar hur man filtrerar rubriker som visas i navigeringspanelen i ett sparat Epub-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke som vi formaterar med en "Rubrik"-stil kan fungera som en rubrik.
// Varje rubrik kan också ha en rubriknivå, som bestäms av numret på dess rubrikstil.
// Rubrikerna nedan är av nivå 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Epub-läsare skapar vanligtvis en innehållsförteckning för sina dokument.
// Varje stycke med stilen "Rubrik" i dokumentet kommer att skapa en post i den här innehållsförteckningen.
  // Vi kan använda egenskapen "EpubNavigationMapLevel" för att ställa in en maximal rubriknivå.
// Epub-läsaren lägger inte till rubriker med en nivå över den vi anger i innehållstabellen.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Vårt dokument har sex rubriker, varav två är över nivå 2.
// Innehållsförteckningen för detta dokument kommer att ha fyra poster.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


