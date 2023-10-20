---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Aspose.Words.Font klass. Innehåller teckensnittsattribut teckensnittsnamn teckenstorlek färg och så vidare för ett objekt i C#.
type: docs
weight: 2830
url: /sv/net/aspose.words/font/
---
## Font class

Innehåller teckensnittsattribut (teckensnittsnamn, teckenstorlek, färg och så vidare) för ett objekt.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class Font
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | Sant om teckensnittet är formaterat med stora bokstäver. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | Returnerar den aktuella beräknade färgen på texten (svart eller vit) som ska användas för 'autofärg'. Om färgen inte är 'auto' returneras[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Anger om innehållet i denna körning ska ha höger-till-vänster-egenskaper. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | Sant om teckensnittet är formaterat med fet stil. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | Sant om texten från höger till vänster är formaterad som fetstil. |
| [Border](../../aspose.words/font/border/) { get; } | Returnerar en[`Border`](../border/) objekt som anger kant för teckensnittet. |
| [Color](../../aspose.words/font/color/) { get; set; } | Hämtar eller ställer in färgen på teckensnittet. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Anger om innehållet i denna körning ska behandlas som komplex skripttext oavsett deras Unicode-teckenvärden när formateringen för denna körning bestäms. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | Sant om teckensnittet är formaterat som dubbel genomstruken text. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | True om teckensnittet är formaterat som relief. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Hämtar eller ställer in betoningen som appliceras på denna formatering. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | Sant om teckensnittet är formaterat som graverat. |
| [Fill](../../aspose.words/font/fill/) { get; } | Får fyllningsformatering för`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | Sant om teckensnittet är formaterat som dold text. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Hämtar eller ställer in markeringsfärgen. |
| [Italic](../../aspose.words/font/italic/) { get; set; } | Sant om teckensnittet är formaterat som kursivt. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | Sant om texten från höger till vänster är formaterad som kursiv. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Hämtar eller ställer in teckenstorleken vid vilken kerning startar. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Returnerar radavstånd för detta teckensnitt (i punkter). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Hämtar eller ställer in lokalidentifieraren (språket) för de formaterade tecknen. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Hämtar eller ställer in lokalidentifieraren (språket) för de formaterade höger-till-vänster-tecken. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Hämtar eller ställer in lokalidentifieraren (språket) för de formaterade asiatiska tecknen. |
| [Name](../../aspose.words/font/name/) { get; set; } | Hämtar eller ställer in namnet på teckensnittet. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Returnerar eller ställer in teckensnittet som används för latinsk text (tecken med teckenkoder från 0 (noll) till 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Returnerar eller ställer in namnet på teckensnittet i ett dokument på höger-till-vänster-språk. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Returnerar eller ställer in ett östasiatiskt teckensnittsnamn. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | Returnerar eller ställer in teckensnittet som används för tecken med teckenkoder från 128 till 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Sant när de formaterade tecknen inte ska stavningskontrolleras. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | Sant om teckensnittet är formaterat som kontur. |
| [Position](../../aspose.words/font/position/) { get; set; } | Hämtar eller ställer in textens position (i punkter) i förhållande till baslinjen. Ett positivt tal höjer texten och ett negativt tal sänker den. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Hämtar eller ställer in teckenbreddsskalning i procent. |
| [Shading](../../aspose.words/font/shading/) { get; } | Returnerar en[`Shading`](../shading/) objekt som hänvisar till skuggformateringen för teckensnittet. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | Sant om teckensnittet är formaterat som skuggat. |
| [Size](../../aspose.words/font/size/) { get; set; } | Hämtar eller ställer in teckenstorleken i poäng. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Hämtar eller ställer in teckenstorleken i punkter som används i ett dokument från höger till vänster. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | Sant om teckensnittet är formaterat som små versaler. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Anger om det aktuella teckensnittet ska använda dokumenttecknen per rad settings vid layout. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Returnerar eller ställer in avståndet (i punkter) mellan tecknen . |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | Sant om teckensnittet är formaterat som genomstruken text. |
| [Style](../../aspose.words/font/style/) { get; set; } | Hämtar eller ställer in teckenstilen som tillämpas på denna formatering. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Hämtar eller ställer in den språkoberoende stilidentifieraren för teckenstilen som tillämpas på denna formatering. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Hämtar eller ställer in namnet på teckenstilen som tillämpas på denna formatering. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | True om teckensnittet är formaterat som subscript. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | Sant om teckensnittet är formaterat som upphöjt. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Får eller ställer in teckensnittsanimeringseffekten. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Hämtar eller ställer in temafärgen i det tillämpade färgschemat som är associerat med detta`Font` objekt. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Hämtar eller ställer in temateckensnittet i det tillämpade teckensnittsschemat som är associerat med detta`Font` objekt. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Hämtar eller ställer in temateckensnittet som används för latinsk text (tecken med teckenkoder från 0 (noll) till 127) i det tillämpade teckensnittsschemat som är associerat med detta`Font` objekt. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Hämtar eller ställer in temateckensnittet i det tillämpade teckensnittsschemat som är associerat med detta`Font` object i ett dokument på höger-till-vänster-språk. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Hämtar eller ställer in det östasiatiska temafonten i det tillämpade teckensnittsschemat som är associerat med detta`Font` objekt. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Hämtar eller ställer in temateckensnittet som används för tecken med teckenkoder från 128 till 255 i det tillämpade teckensnittsschemat som är associerat med detta`Font` objekt. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelt värde som gör en färg ljusare eller mörkare. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Hämtar eller ställer in typen av understrykning som appliceras på teckensnittet. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Hämtar eller ställer in färgen på understrykningen som appliceras på teckensnittet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Återställer till standardtypsnittsformatering. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | Kontrollerar om en viss DrawingML-texteffekt tillämpas. |

## Anmärkningar

Du skapar inte instanser av`Font`klass direkt. Du använder bara `Font` för att komma åt teckensnittsegenskaperna för de olika objekten som t.ex[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

## Exempel

Visar hur man formaterar en serie text med dess teckensnittsegenskap.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Visar hur man infogar en sträng omgiven av en kant i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Visar hur du skapar och använder ett styckeformat med listformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en anpassad styckestil.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Skapa en lista och se till att styckena som använder den här stilen kommer att använda den här listan.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Använd styckeformatet på dokumentbyggarens nuvarande stycke och lägg sedan till lite text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändra dokumentbyggarens stil till en som inte har någon listformatering och skriv ett stycke till.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
