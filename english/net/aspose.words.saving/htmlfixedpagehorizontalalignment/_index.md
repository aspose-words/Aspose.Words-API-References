---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.HtmlFixedPageHorizontalAlignment enum for precise control of page alignment in your HTML documents. Enhance your document formatting today!
type: docs
weight: 5810
url: /net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Specifies the horizontal alignment for pages in output HTML document.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | Align pages to the left. |
| Center | `1` | Center pages. This is the default value. |
| Right | `2` | Align pages to the right. |

## Examples

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.That(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success, Is.True);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.That(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success, Is.True);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.That(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success, Is.True);
        break;
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
