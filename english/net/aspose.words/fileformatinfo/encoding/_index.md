---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: Discover the FileFormatInfo Encoding property to identify document encoding effortlessly. Currently supports HTML formats for accurate results.
type: docs
weight: 10
url: /net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents.

```csharp
public Encoding Encoding { get; }
```

## Examples

Shows how to detect encoding in an html file.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.That(info.LoadFormat, Is.EqualTo(LoadFormat.Html));

// The Encoding property is used only when we create a FileFormatInfo object for an html document.
// On Windows, the detected ISO-8859-1 encoding is reported as its Windows-1252 superset.
Assert.That(info.Encoding.EncodingName, Is.EqualTo(isLinux ? "Western European (ISO)" : "Western European (Windows)"));
Assert.That(info.Encoding.CodePage, Is.EqualTo(isLinux ? 28591 : 1252));
```

### See Also

* class [FileFormatInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
