---
title: HeaderFooter.IsLinkedToPrevious
linktitle: IsLinkedToPrevious
articleTitle: IsLinkedToPrevious
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen IsLinkedToPrevious förbättrar dokumentets sidhuvuden och sidfötter, vilket säkerställer sömlös kontinuitet över avsnitt för bättre organisation.
type: docs
weight: 40
url: /sv/net/aspose.words/headerfooter/islinkedtoprevious/
---
## HeaderFooter.IsLinkedToPrevious property

Sant om detta sidhuvud eller sidfot är länkat till motsvarande sidhuvud eller sidfot i föregående avsnitt.

```csharp
public bool IsLinkedToPrevious { get; set; }
```

## Anmärkningar

Standard är`sann`.

Observera att när din länk är en sidhuvud eller sidfot rensas dess innehåll.

## Exempel

Visar hur man länkar sidhuvuden och sidfot mellan avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Gå till den första sektionen och skapa ett sidhuvud och en sidfot. Som standard,
// sidhuvudet och sidfoten visas bara på sidor i den sektion som innehåller dem.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Vi kan länka ett avsnitts sidhuvuden/sidfot till föregående avsnitts sidhuvuden/sidfot
// för att tillåta att den länkande sektionen visar den länkade sektionens sidhuvuden/sidfot.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Varje sektion kommer fortfarande att ha sina egna sidhuvud-/sidfotsobjekt. När vi länkar sektioner,
// den länkande sektionen visar den länkade sektionens sidhuvud/sidfot men behåller sina egna.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Länka sidhuvuden/sidfötterna i det tredje avsnittet till sidhuvuden/sidfötterna i det andra avsnittet.
// Det andra avsnittet länkar redan till det första avsnittets sidhuvud/sidfot,
// så att länka till den andra sektionen skapar en länkkedja.
// Den första, andra och nu den tredje sektionen kommer alla att visa den första sektionens rubriker.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Vi kan ta bort länken till ett tidigare avsnitts sidhuvud/sidfot genom att skicka "false" när vi anropar LinkToPrevious-metoden.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Vi kan också välja att bara länka en specifik typ av sidhuvud/sidfot med den här metoden.
// Den tredje sektionen kommer nu att ha samma sidfot som den andra och första sektionen, men inte sidhuvudet.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Det första avsnittets sidhuvud/sidfot kan inte länka sig till någonting eftersom det inte finns något föregående avsnitt.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Alla sidhuvuden/sidfoter i det andra avsnittet är länkade till sidhuvuden/sidfoter i det första avsnittet.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// I det tredje avsnittet är endast sidfoten länkad till det första avsnittets sidfot via det andra avsnittet.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Se även

* class [HeaderFooter](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
