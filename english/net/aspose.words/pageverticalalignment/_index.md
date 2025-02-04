---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.PageVerticalAlignment enum. Specifies vertical justification of text on each page in C#.
type: docs
weight: 4960
url: /net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

Specifies vertical justification of text on each page.

```csharp
public enum PageVerticalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Bottom | `3` | Text is aligned at the bottom of the page. |
| Center | `1` | Text is aligned in the middle of the page. |
| Justify | `2` | Text is spread to fill the page. |
| Top | `0` | Text is aligned at the top of the page. |

## Examples

Shows how to apply and revert page setup settings to sections in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modify the page setup properties for the builder's current section and add text.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### See Also

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
