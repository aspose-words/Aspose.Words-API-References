---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words för .NET
description: Upptäck HtmlSaveOptions NavigationMapLevel-egenskap, som styr rubriknivåer i EPUB-, MOBI- och AZW3-exporter. Maximera ditt innehålls synlighet!
type: docs
weight: 390
url: /sv/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Anger den maximala nivån av rubriker som fylls i navigeringskartan vid export till EPUB-, MOBI- eller AZW3 -format. Standardvärdet är`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Anmärkningar

Navigeringskartan gör det möjligt för användaragenter att enkelt navigera genom dokumentstrukturen. Vanligtvis motsvarar navigeringspunkter rubriker i dokumentet. För att fylla i rubriker upp till nivå**N** tilldela detta värde till`NavigationMapLevel`.

Som standard är tre nivåer av rubriker ifyllda: stycken med formatmallar**Rubrik 1** ,**Rubrik 2** och**Rubrik 3**. Du kan ställa in den här egenskapen på ett värde från 1 till 9 för att begära motsvarande maximala nivå. Om du ställer in den på noll reduceras navigeringskartan till endast dokumentroten eller rötterna för dokumentdelarna.

## Exempel

Visar hur man genererar innehållsförteckningar för Azw3-dokument.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Visar hur man genererar innehållsförteckningar för Mobi-dokument.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Visar hur man filtrerar rubriker som visas i navigeringspanelen i ett sparat Epub-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke som vi formaterar med formatet "Rubrik" kan fungera som en rubrik.
// Varje rubrik kan också ha en rubriknivå, bestämd av numret på dess rubrikstil.
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
// Varje stycke med formatet "Rubrik" i dokumentet skapar en post i innehållsförteckningen.
 // Vi kan använda egenskapen "NavigationMapLevel" för att ange en maximal rubriknivå.
// Epub-läsaren lägger inte till rubriker med en nivå över den vi anger i innehållstabellen.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// Vårt dokument har sex rubriker, varav två är över nivå 2.
// Innehållsförteckningen för detta dokument kommer att ha fyra poster.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
