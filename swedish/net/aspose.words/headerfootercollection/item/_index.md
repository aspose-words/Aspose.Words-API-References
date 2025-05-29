---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till sidhuvuden eller sidfot med egenskapen Item. Hämta specifika sidhuvuden eller sidfot via index för effektiv dokumenthantering.
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
| index | Ett index till samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

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
| headerFooterType | En[`HeaderFooterType`](../../headerfootertype/) värde som anger vilken typ av sidhuvud/sidfot som ska hämtas. |

## Anmärkningar

Returer`null`om sidhuvudet/sidfoten av den angivna typen inte hittas.

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

Visar hur man tar bort alla sidfot från ett dokument.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Gå igenom varje avsnitt och ta bort sidfot av alla slag.
foreach (Section section in doc.OfType<Section>())
{
    // Det finns tre typer av sidfot och sidhuvud.
    // 1 - Sidhuvudet/sidfoten "Första", som bara visas på första sidan i ett avsnitt.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Sidhuvudet/sidfoten "Primärt", som visas på udda sidor.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Sidhuvudet/sidfoten "Jämnt", som visas på jämna sidor.
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
