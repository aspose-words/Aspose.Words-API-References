---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup EndnoteOptions för att enkelt anpassa numrering och placering av slutnoter för förbättrad dokumentformatering och tydlighet.
type: docs
weight: 120
url: /sv/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Ger alternativ som styr numrering och placering av slutnoter i det här avsnittet.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Exempel

Visar hur man konfigurerar alternativ som påverkar fotnoter/slutnoter i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Konfigurera alla fotnoter i det första avsnittet för att börja om numreringen från 1
// på varje ny sida och visas direkt under texten på varje sida.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Konfigurera alla slutnoter i det första avsnittet för att upprätthålla en kontinuerlig räkning genom hela avsnittet,
// med början från 1. Ställ också in dem så att de alla visas samlade i slutet av dokumentet.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Se även

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
