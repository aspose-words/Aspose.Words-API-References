---
title: SectionStart Enum
linktitle: SectionStart
articleTitle: SectionStart
second_title: Aspose.Words for .NET
description: Aspose.Words.SectionStart enum. The type of break at the beginning of the section in C#.
type: docs
weight: 5760
url: /net/aspose.words/sectionstart/
---
## SectionStart enumeration

The type of break at the beginning of the section.

```csharp
public enum SectionStart
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Continuous | `0` | The new section starts on the same page as the previous section. |
| NewColumn | `1` | The section starts from a new column. |
| NewPage | `2` | The section starts from a new page. |
| EvenPage | `3` | The section starts on a new even page. |
| OddPage | `4` | The section starts on a new odd page. |

## Examples

Shows how to specify how a new section separates itself from the previous.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Section break types determine how a new section separates itself from the previous section.
// Below are five types of section breaks.
// 1 -  Starts the next section on a new page:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 -  Starts the next section on the current page:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 -  Starts the next section on a new even page:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 -  Starts the next section on a new odd page:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 -  Starts the next section on a new column:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
