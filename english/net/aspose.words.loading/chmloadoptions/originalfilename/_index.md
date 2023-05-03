---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
second_title: Aspose.Words for .NET API Reference
description: ChmLoadOptions OriginalFileName property. The name of the CHM file. Default value is null in C#.
type: docs
weight: 20
url: /net/aspose.words.loading/chmloadoptions/originalfilename/
---
## OriginalFileName property

The name of the CHM file. Default value is `null`.

```csharp
public string OriginalFileName { get; set; }
```

## Remarks

CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links and normally uses [`OriginalFileName`](../../../aspose.words/document/originalfilename/) to check whether the file referenced by a link is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified explicitly via this property, since it cannot be determined automatically.

If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take priority over the actual name of the file stored in [`OriginalFileName`](../../../aspose.words/document/originalfilename/).

## Examples

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```csharp
// Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
// so file links don't work after saving it to HTML.
// We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### See Also

* class [ChmLoadOptions](../)
* namespace [Aspose.Words.Loading](../../chmloadoptions/)
* assembly [Aspose.Words](../../../)
