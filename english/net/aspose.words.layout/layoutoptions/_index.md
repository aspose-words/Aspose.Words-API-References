---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Layout.LayoutOptions to optimize document layout control, enhancing your Word processing experience with flexible customization options.
type: docs
weight: 3800
url: /net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Holds the options that allow controlling the document layout process.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) documentation article.

```csharp
public class LayoutOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Gets or sets [`IPageLayoutCallback`](../ipagelayoutcallback/) implementation used by page layout model. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Gets or sets the way comments are rendered. Default value is ShowInBalloons. |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is `true`. |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Gets or sets an indication of whether the original font metrics should be used after font substitution. Default is `true`. |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Gets revision options. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Gets or sets indication of whether hidden text in the document is rendered. Default is `false`. |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Gets or sets indication of whether paragraph marks are rendered. Default is `false`. |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Gets or sets [`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) implementation used for Advanced Typography rendering features. |

## Remarks

You do not create instances of this class directly. Use the [`LayoutOptions`](../../aspose.words/document/layoutoptions/) property to access layout options for this document.

Note that after changing any of the options present in this class, [`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) method should be called in order for the changed options to be applied to the layout.

## Examples

Shows how to hide text in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Shows how to show paragraph marks in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
// with a pilcrow (¶) symbol when we render the document.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Shows how to alter the appearance of revisions in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a revision, then change the color of all revisions to green.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
