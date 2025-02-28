---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words for .NET
description: Discover the ChmLoadOptions constructor for seamless initialization. Set default values effortlessly and enhance your application's performance today!
type: docs
weight: 10
url: /net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Initializes a new instance of this class with default values.

```csharp
public ChmLoadOptions()
```

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
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
