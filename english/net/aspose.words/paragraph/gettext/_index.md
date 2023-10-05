---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Paragraph GetText method. Gets the text of this paragraph including the end of paragraph character in C#.
type: docs
weight: 280
url: /net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Gets the text of this paragraph including the end of paragraph character.

```csharp
public override string GetText()
```

## Remarks

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:

* If the paragraph is the last paragraph of [`Body`](../../body/), then [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [`Cell`](../../../aspose.words.tables/cell/), then [`Cell`](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) is appended.

The returned string includes all control and special characters as described in [`ControlChar`](../../controlchar/).

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
