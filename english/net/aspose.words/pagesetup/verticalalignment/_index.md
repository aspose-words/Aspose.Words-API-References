---
title: PageSetup.VerticalAlignment
second_title: Aspose.Words for .NET API Reference
description: PageSetup property. Returns or sets the vertical alignment of text on each page in a document or section in C#.
type: docs
weight: 450
url: /net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Returns or sets the vertical alignment of text on each page in a document or section.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

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

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
