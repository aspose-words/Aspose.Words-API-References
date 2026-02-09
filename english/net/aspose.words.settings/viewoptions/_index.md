---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Settings.ViewOptions class to customize document display in Microsoft Word, enhancing your editing experience and productivity.
type: docs
weight: 6860
url: /net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Provides various options that control how a document is shown in Microsoft Word.

To learn more, visit the [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) documentation article.

```csharp
public class ViewOptions
```

## Properties

| Name | Description |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Controls display of the background shape in print layout view. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Turns off display of the space between the top of the text and the top edge of the page. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Specifies whether the document is in forms design mode. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Controls the view mode in Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Gets or sets the percentage at which you want to view your document. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Gets or sets a zoom value based on the size of the window. |

## Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.That(doc.ViewOptions.ZoomType, Is.EqualTo(ZoomType.Custom));
Assert.That(doc.ViewOptions.ZoomType, Is.EqualTo(ZoomType.None));

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
// to automatically zoom the document to fit the width of the page.
// Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
// to automatically zoom the document to make the entire first page visible.
// Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
// to automatically zoom the document to fit the inner text margins of the first page.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### See Also

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
