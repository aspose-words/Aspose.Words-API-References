---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words for .NET API Reference
description: Section PrependContent method. Inserts a copy of content of the source section at the beginning of this section in C#.
type: docs
weight: 140
url: /net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Inserts a copy of content of the source section at the beginning of this section.

```csharp
public void PrependContent(Section sourceSection)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | Section | The section to copy content from. |

## Remarks

Only content of [`Body`](../body/) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

## Examples

Shows how to append the contents of a section to another section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// Insert the contents of the first section to the beginning of the third section.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Insert the contents of the second section to the end of the third section.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// The "PrependContent" and "AppendContent" methods did not create any new sections.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../section/)
* assembly [Aspose.Words](../../../)
