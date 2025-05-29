---
title: EndnoteOptions.RestartRule
linktitle: RestartRule
articleTitle: RestartRule
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen EndnoteOptions RestartRule förbättrar ditt dokument genom att styra automatisk numrering för ett elegant och professionellt utseende.
type: docs
weight: 30
url: /sv/net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

Avgör när automatisk numrering startar om.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

## Anmärkningar

Inte alla värden är tillämpliga på slutnoter. För att fastställa vilka värden som är tillämpliga, se[`FootnoteNumberingRule`](../../footnotenumberingrule/).

## Exempel

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

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
