---
title: XpsSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: XpsSaveOptions CompressionLevel property. Specifies the compression level used to save document. The default value is Normal.
type: docs
weight: 20
url: /net/aspose.words.saving/xpssaveoptions/compressionlevel/
---
## XpsSaveOptions.CompressionLevel property

Specifies the compression level used to save document. The default value is Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Examples

Shows how to control the compression level when saving a document to XPS format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample document for XPS compression test.");

// Create an XpsSaveOptions object and set the compression level.
XpsSaveOptions options = new XpsSaveOptions();
options.CompressionLevel = CompressionLevel.Maximum;

doc.Save(ArtifactsDir + "XpsSaveOptions.CompressionLevelXps.xps", options);
```

### See Also

* enum [CompressionLevel](../../compressionlevel/)
* class [XpsSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
