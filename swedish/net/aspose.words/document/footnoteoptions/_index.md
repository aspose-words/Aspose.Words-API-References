---
title: FootnoteOptions
second_title: Aspose.Words för .NET API Referens
description: Ger alternativ som styr numrering och placering av fotnoter i detta dokument.
type: docs
weight: 150
url: /sv/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Ger alternativ som styr numrering och placering av fotnoter i detta dokument.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### Exempel

Visar hur du väljer en annan plats där dokumentet samlas in och visar dess fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En fotnot är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör flödet i huvudtexten.  
// Att infoga en fotnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar fotnoten.
// Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Vi kan använda egenskapen "Position" för att bestämma var dokumentet ska placera alla dess fotnoter.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BottomOfPage",
// varje fotnot kommer att dyka upp längst ner på sidan som innehåller dess referensmärke. Detta är standardvärdet.
// Om vi ställer in värdet på egenskapen "Position" till "FootnotePosition.BeneathText",
// varje fotnot kommer att dyka upp i slutet av sidans text som innehåller dess referensmärke.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Visar hur man ställer in ett nummer vid vilket dokumentet börjar räkna fotnot/slutnot.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör flödet i huvudtexten. 
// Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnotsposter visas som standard längst ner på varje sida som innehåller
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
// för fotnoter och för slutnoter, som båda börjar på 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Vi kan använda egenskapen "StartNumber" för att få dokumentet till
// börjar räkna en fotnot eller slutnot med ett annat nummer.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Visar hur man ändrar nummerstilen för fotnots-/slutnotsreferensmärken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör flödet i huvudtexten. 
// Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
// symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnotsposter visas som standard längst ner på varje sida som innehåller
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
// för fotnoter och för slutnoter. Som standard visar fotnoter deras nummer med arabiska siffror,
// och slutnoter visar sina nummer med gemener romerska siffror.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Vi kan använda egenskapen "NumberStyle" för att tillämpa anpassade numreringsstilar på fotnoter och slutnoter.
// Detta kommer inte att påverka fotnoter/slutnoter med anpassade referensmärken.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Visar hur man startar om fotnots-/slutnotsnumrering på vissa ställen i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text
// som inte stör flödet i huvudtexten. 
// Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
// symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnotsposter visas som standard längst ner på varje sida som innehåller
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
// för fotnoter och slutnoter och startar inte om dessa räkningar vid något tillfälle.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Vi kan använda egenskapen "RestartRule" för att få dokumentet att starta om
// fotnoten/slutnoten räknas på en ny sida eller sektion.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Se även

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
