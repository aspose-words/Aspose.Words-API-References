---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.ChapterPageSeparator enum to customize chapter and page number separators for enhanced document formatting and clarity.
type: docs
weight: 390
url: /net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Defines the separator character that appears between the chapter and page number.

```csharp
public enum ChapterPageSeparator
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Hyphen | `0` | A colon. |
| Period | `1` | A period. |
| Colon | `2` | A colon. |
| EmDash | `3` | An emphasized dash. |
| EnDash | `4` | A standard dash. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
