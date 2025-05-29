---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.FootnoteOptions för anpassningsbar fotnotsnumrering i dina dokument och avsnitt. Förbättra dokumentets tydlighet idag!
type: docs
weight: 4970
url: /sv/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Representerar fotnotsnumreringsalternativen för ett dokument eller avsnitt.

För att lära dig mer, besök[Arbeta med fotnot och slutnot](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) dokumentationsartikel.

```csharp
public sealed class FootnoteOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Anger antalet kolumner som fotnotsområdet formateras med. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Anger numreringsformatet för automatiskt numrerade fotnoter. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Anger fotnoternas position. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Avgör när automatisk numrering startar om. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | Anger startnumret eller tecknet för de första automatiskt numrerade fotnoterna. |

## Exempel

Visar hur man delar upp fotnotsavsnittet i ett givet antal kolumner.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

Visar hur man väljer en annan plats där dokumentet samlas och visar sina fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En fotnot är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot läggs en liten upphöjd referenssymbol till
// vid huvudtexten där vi infogar fotnoten.
// Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens metod "InsertFootnote".
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Vi kan använda egenskapen "Position" för att avgöra var dokumentet ska placera alla sina fotnoter.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BottomOfPage",
// varje fotnot visas längst ner på sidan som innehåller dess referensmarkering. Detta är standardvärdet.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BeneathText",
// varje fotnot kommer att visas i slutet av sidans text som innehåller dess referensmarkering.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Visar hur man anger ett nummer där dokumentet börjar fotnots-/slutnoträkningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot/slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnoter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler och slutnoter visas i slutet av dokumentet.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument har separata räkningar
// för fotnoter och slutnoter, som båda börjar på 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Vi kan använda egenskapen "StartNumber" för att få dokumentet att
// börjar en fotnots- eller slutnoträkning vid ett annat nummer.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Visar hur man ändrar numreringsstilen för referensmarkeringar i fotnoter/slutnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot/slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
// symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnoter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler och slutnoter visas i slutet av dokumentet.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument har separata räkningar
// för fotnoter och slutnoter. Som standard visas fotnoters nummer med arabiska siffror,
// och slutnoter visar sina nummer med gemena romerska siffror.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Vi kan använda egenskapen "NumberStyle" för att tillämpa anpassade numreringsstilar på fotnoter och slutnoter.
// Detta påverkar inte fotnoter/slutnoter med anpassade referensmarkeringar.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Visar hur man börjar om fotnots-/slutnotsnumrering på vissa ställen i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot/slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
// symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnoter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler och slutnoter visas i slutet av dokumentet.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument har separata räkningar
// för fotnoter och slutnoter och startar inte om dessa räkningar någon gång.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Vi kan använda egenskapen "RestartRule" för att få dokumentet att starta om
// fotnoten/slutnoten räknas vid en ny sida eller ett nytt avsnitt.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Se även

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)
