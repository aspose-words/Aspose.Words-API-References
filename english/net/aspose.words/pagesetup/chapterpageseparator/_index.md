---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words for .NET API Reference
description: PageSetup ChapterPageSeparator property. Gets or sets the separator character that appears between the chapter number and the page number in C#.
type: docs
weight: 90
url: /net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Gets or sets the separator character that appears between the chapter number and the page number.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Remarks

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

## Examples

Shows how to work with page chapters.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### See Also

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
