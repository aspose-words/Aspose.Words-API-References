---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words for .NET
description: Discover HtmlLoadOptions' WebRequestTimeout property, allowing you to customize timeout settings for optimal web performance. Default, 100 seconds.
type: docs
weight: 80
url: /net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds).

```csharp
public int WebRequestTimeout { get; set; }
```

## Remarks

The number of milliseconds that Aspose.Words waits for a response, when loading external resources (images, style sheets) linked in HTML and MHTML documents.

## Examples

Shows how to set a time limit for web requests when loading a document with external resources linked by URLs.

```csharp
public void WebRequestTimeout()
{
    // Create a new HtmlLoadOptions object and verify its timeout threshold for a web request.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // When loading an Html document with resources externally linked by a web address URL,
    // Aspose.Words will abort web requests that fail to fetch the resources within this time limit, in milliseconds.
    Assert.That(options.WebRequestTimeout, Is.EqualTo(100000));

    // Set a WarningCallback that will record all warnings that occur during loading.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Load such a document and verify that a shape with image data has been created.
    // This linked image will require a web request to load, which will have to complete within our time limit.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Set an unreasonable timeout limit and try load the document again.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.That(warningCallback.Warnings().Count, Is.EqualTo(2));

    // A web request that fails to obtain an image within the time limit will still produce an image.
    // However, the image will be the red 'x' that commonly signifies missing images.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.That(imageShape.ImageData.ImageBytes.Length, Is.EqualTo(924));

    // We can also configure a custom callback to pick up any warnings from timed out web requests.
    Assert.That(warningCallback.Warnings()[0].Source, Is.EqualTo(WarningSource.Html));
    Assert.That(warningCallback.Warnings()[0].WarningType, Is.EqualTo(WarningType.DataLoss));
    Assert.That(warningCallback.Warnings()[0].Description, Is.EqualTo($"Couldn't load a resource from \'{ImageUrl}\'."));

    Assert.That(warningCallback.Warnings()[1].Source, Is.EqualTo(WarningSource.Html));
    Assert.That(warningCallback.Warnings()[1].WarningType, Is.EqualTo(WarningType.DataLoss));
    Assert.That(warningCallback.Warnings()[1].Description, Is.EqualTo("Image has been replaced with a placeholder."));

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Stores all warnings that occur during a document loading operation in a List.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### See Also

* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
