---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words for .NET
description: Discover how the PageSetup RtlGutter property in Microsoft Word optimizes section layouts for right-to-left and left-to-right languages. Enhance your document design!
type: docs
weight: 380
url: /net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.

```csharp
public bool RtlGutter { get; set; }
```

## Examples

Shows how to set gutter margins.

```csharp
Document doc = new Document();

// Insert text that spans several pages.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// A gutter adds whitespaces to either the left or right page margin,
// which makes up for the center folding of pages in a book encroaching on the page's layout.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Determine how much space our pages have for text within the margins and then add an amount to pad a margin. 
Assert.That(pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, Is.EqualTo(470.30d).Within(0.01d));

pageSetup.Gutter = 100.0d;

// Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
pageSetup.RtlGutter = true;

// Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
// the left/right page side position of margins every page.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
