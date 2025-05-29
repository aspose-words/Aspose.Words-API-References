---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChapterPageSeparator i PageSetup. Anpassa enkelt avgränsartecknet mellan kapitel- och sidnummer för ett elegant utseende.
type: docs
weight: 90
url: /sv/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Hämtar eller anger avgränsartecknet som visas mellan kapitelnumret och sidnumret.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Anmärkningar

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
