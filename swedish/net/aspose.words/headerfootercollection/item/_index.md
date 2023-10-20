---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: HeaderFooterCollection Item fast egendom. Hämtar enHeaderFooter vid det givna indexet i C#.
type: docs
weight: 10
url: /sv/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Hämtar en[`HeaderFooter`](../../headerfooter/) vid det givna indexet.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index i samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från baksidan av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder näst före sist och så vidare.

Om index är större än eller lika med antalet objekt i listan, returnerar detta en nollreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returnerar detta en nollreferens.

## Exempel

Visar hur du länkar sidhuvuden och sidfötter mellan avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Flytta till det första avsnittet och skapa ett sidhuvud och en sidfot. Som standard,
// sidhuvudet och sidfoten kommer bara att visas på sidorna i avsnittet som innehåller dem.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Vi kan länka ett avsnitts sidhuvuden/sidfötter till föregående avsnitts sidhuvuden/sidfötter
// för att tillåta länkningssektionen att visa den länkade sektionens sidhuvuden/sidfötter.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Varje sektion kommer fortfarande att ha sina egna sidhuvuds-/sidfotsobjekt. När vi länkar avsnitt,
// länksektionen kommer att visa den länkade sektionens sidhuvud/sidfötter samtidigt som den behåller sin egen.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Länka sidhuvuden/sidfötter i det tredje avsnittet till sidhuvuden/sidfötter i det andra avsnittet.
// Det andra avsnittet länkar redan till det första avsnittets sidhuvud/sidfötter,
// så att länka till den andra sektionen skapar en länkkedja.
// Den första, andra och nu tredje sektionen kommer alla att visa den första sektionens rubriker.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Vi kan ta bort länken till ett tidigare avsnitts sidhuvud/sidfötter genom att skicka "false" när vi anropar LinkToPrevious-metoden.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Vi kan också välja endast en specifik typ av sidhuvud/sidfot att länka med den här metoden.
// Det tredje avsnittet kommer nu att ha samma sidfot som det andra och första avsnittet, men inte sidhuvudet.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Det första avsnittets sidhuvud/sidfot kan inte länka sig till någonting eftersom det inte finns något tidigare avsnitt.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Alla det andra avsnittets sidhuvud/sidfötter är länkade till det första avsnittets sidhuvuden/sidfötter.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// I den tredje sektionen är endast sidfoten länkad till den första sektionens sidfot via den andra sektionen.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Se även

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Hämtar en[`HeaderFooter`](../../headerfooter/) av den angivna typen.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| headerFooterType | A[`HeaderFooterType`](../../headerfootertype/) värde som anger typen av sidhuvud/sidfot som ska hämtas. |

## Anmärkningar

Returnerar`null` om sidhuvudet/sidfoten av den angivna typen inte hittas.

## Exempel

Visar hur man ersätter text i ett dokuments sidfot.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Visar hur man tar bort alla sidfötter från ett dokument.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterera genom varje avsnitt och ta bort sidfötter av alla slag.
foreach (Section section in doc.OfType<Section>())
{
    // Det finns tre typer av sidfots- och sidhuvudstyper.
    // 1 - Den "Första" sidhuvudet/sidfoten, som bara visas på första sidan i ett avsnitt.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Den "Primära" sidhuvudet/sidfoten, som visas på udda sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - "Jämn" sidhuvudet/sidfoten, som visas på jämna sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Se även

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
