---
title: Document.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words för .NET
description: Utforska egenskapen EndnoteOptions för att anpassa numrering och placering av slutnoter, vilket förbättrar dokumentets tydlighet och professionalism.
type: docs
weight: 120
url: /sv/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Ger alternativ som styr numrering och placering av slutnoter i det här dokumentet.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Exempel

Visar hur man väljer en annan plats där dokumentet samlar in och visar sina slutnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En slutnot är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar slutnoten.
// Varje slutnot skapar också en post i slutet av dokumentet, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Vi kan använda egenskapen "Position" för att avgöra var dokumentet ska placera alla sina slutnoter.
// Om vi ställer in värdet för egenskapen "Position" till "EndnotePosition.EndOfDocument",
// varje fotnot kommer att visas i en samling i slutet av dokumentet. Detta är standardvärdet.
// Om vi ställer in värdet för egenskapen "Position" till "EndnotePosition.EndOfSection",
// varje fotnot kommer att visas i en samling i slutet av det avsnitt vars text innehåller slutnotens referensmarkering.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
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

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
