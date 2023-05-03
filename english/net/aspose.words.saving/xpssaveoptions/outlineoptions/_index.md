---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
second_title: Aspose.Words for .NET API Reference
description: XpsSaveOptions OutlineOptions property. Allows to specify outline options in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## OutlineOptions property

Allows to specify outline options.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Remarks

Note that [`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) option will not work when saving to XPS.

## Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// The output XPS document will contain an outline, a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### See Also

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* namespace [Aspose.Words.Saving](../../xpssaveoptions/)
* assembly [Aspose.Words](../../../)
