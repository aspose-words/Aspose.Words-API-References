---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup HeadingLevelForChapter för att enkelt anpassa kapitelrubrikstilar i ditt dokument för förbättrad läsbarhet och professionalism.
type: docs
weight: 180
url: /sv/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Hämtar eller ställer in den rubriknivåstil som tillämpas på kapiteltitlarna i dokumentet.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Anmärkningar

Kan vara ett tal från 0 till 9. 0 betyder inget kapitelnummer om det används på sidnumret.

Innan du kan skapa sidnummer som inkluderar kapitelnummer måste dokumentrubrikerna ha ett numrerat dispositionsformat tillämpat.

## Exempel

Visar hur man arbetar med sidkapitel.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
