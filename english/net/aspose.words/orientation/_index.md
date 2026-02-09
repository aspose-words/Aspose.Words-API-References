---
title: Orientation Enum
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Orientation enum for seamless page orientation control. Enhance your document formatting with ease and precision!
type: docs
weight: 5090
url: /net/aspose.words/orientation/
---
## Orientation enumeration

Specifies page orientation.

```csharp
public enum Orientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Portrait | `1` | Portrait page orientation (narrow and tall). |
| Landscape | `2` | Landscape page orientation (wide and short). |

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

Assert.That(doc.Sections[1].PageSetup.Orientation, Is.EqualTo(Orientation.Landscape));
Assert.That(doc.Sections[1].PageSetup.VerticalAlignment, Is.EqualTo(PageVerticalAlignment.Center));

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.PageSetup.ClearFormatting();

Assert.That(doc.Sections[1].PageSetup.Orientation, Is.EqualTo(Orientation.Portrait));
Assert.That(doc.Sections[1].PageSetup.VerticalAlignment, Is.EqualTo(PageVerticalAlignment.Top));

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
