---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words for .NET
description: Enhance your content with the Section PrependContent method, effortlessly inserting source section text at the start for improved organization and clarity.
type: docs
weight: 160
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

Assert.That(section.GetText(), Is.EqualTo("Section 3" + ControlChar.SectionBreak));

// Insert the contents of the first section to the beginning of the third section.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Insert the contents of the second section to the end of the third section.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// The "PrependContent" and "AppendContent" methods did not create any new sections.
Assert.That(doc.Sections.Count, Is.EqualTo(3));
Assert.That(section.GetText(), Is.EqualTo("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak));
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
