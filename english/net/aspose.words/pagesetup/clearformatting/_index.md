---
title: PageSetup.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Reset your document's page setup effortlessly with the ClearFormatting method. Restore default margins, paper size, and orientation for a polished look.
type: docs
weight: 460
url: /net/aspose.words/pagesetup/clearformatting/
---
## PageSetup.ClearFormatting method

Resets page setup to default paper size, margins and orientation.

```csharp
public void ClearFormatting()
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

* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
