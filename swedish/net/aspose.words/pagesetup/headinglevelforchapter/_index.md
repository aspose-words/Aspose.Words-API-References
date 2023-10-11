---
title: PageSetup.HeadingLevelForChapter
second_title: Aspose.Words för .NET API Referens
description: PageSetup fast egendom. Hämtar eller ställer in rubriknivåstilen som tillämpas på kapiteltitlarna i dokumentet.
type: docs
weight: 180
url: /sv/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Hämtar eller ställer in rubriknivåstilen som tillämpas på kapiteltitlarna i dokumentet.

```csharp
public int HeadingLevelForChapter { get; set; }
```

### Anmärkningar

Kan vara ett nummer från 0 till 9. 0 betyder inget kapitelnummer om det tillämpas på sidnummer.

Innan du kan skapa sidnummer som inkluderar kapitelnummer måste dokumentrubrikerna ha ett numrerat dispositionsformat.

### Exempel

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
* namnutrymme [Aspose.Words](../../pagesetup/)
* hopsättning [Aspose.Words](../../../)


