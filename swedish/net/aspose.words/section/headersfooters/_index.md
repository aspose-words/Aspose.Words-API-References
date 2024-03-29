---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: Aspose.Words för .NET
description: Section HeadersFooters fast egendom. Ger åtkomst till noder för sidhuvuden och sidfötter i avsnittet i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Ger åtkomst till noder för sidhuvuden och sidfötter i avsnittet.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

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

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
