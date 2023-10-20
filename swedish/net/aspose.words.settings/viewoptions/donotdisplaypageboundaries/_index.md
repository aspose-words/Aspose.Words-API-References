---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words för .NET
description: ViewOptions DoNotDisplayPageBoundaries fast egendom. Stänger av visningen av utrymmet mellan textens överkant och sidans övre kant i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Stänger av visningen av utrymmet mellan textens överkant och sidans övre kant.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Exempel

Visar hur man döljer vertikala blanksteg och sidhuvuden/sidfötter i vyalternativ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga innehåll som sträcker sig över 3 sidor.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Infoga ett sidhuvud och en sidfot.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Det här dokumentet innehåller en liten mängd innehåll som tar upp ett par helsidor.
// Ställ in flaggan "DoNotDisplayPageBoundaries" till "true" för att få äldre versioner av Microsoft Word att utelämna rubriker,
// sidfötter och mycket av det vertikala blanktecken när vi visar vårt dokument.
// Ställ in "DoNotDisplayPageBoundaries"-flaggan till "false" för att hämta äldre versioner av Microsoft Word
// för att normalt visa vårt dokument.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Se även

* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
