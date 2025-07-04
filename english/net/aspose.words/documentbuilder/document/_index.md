---
title: DocumentBuilder.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Manage Document properties effortlessly with DocumentBuilder. Easily get or set your Document object for streamlined document management.
type: docs
weight: 90
url: /net/aspose.words/documentbuilder/document/
---
## DocumentBuilder.Document property

Gets or sets the `Document` object that this object is attached to.

```csharp
public Document Document { get; set; }
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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
