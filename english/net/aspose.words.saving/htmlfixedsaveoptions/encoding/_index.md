---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: Discover the HtmlFixedSaveOptions Encoding property for seamless HTML exports. Easily set UTF-8 encoding with BOM for optimal data integrity.
type: docs
weight: 30
url: /net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Specifies the encoding to use when exporting to HTML. Default value is `new UTF8Encoding(true)` (UTF-8 with BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Examples

Shows how to set which encoding to use while exporting a document to HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// The default encoding is UTF-8. If we want to represent our document using a different encoding,
// we can use a SaveOptions object to set a specific encoding.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.That(htmlFixedSaveOptions.Encoding.EncodingName, Is.EqualTo("US-ASCII"));

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
