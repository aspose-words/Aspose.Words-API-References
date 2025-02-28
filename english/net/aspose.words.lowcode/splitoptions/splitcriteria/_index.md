---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: Discover how the SplitOptions SplitCriteria property enhances document management by efficiently dividing your content into manageable sections.
type: docs
weight: 20
url: /net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Specifies the criteria for splitting the document into parts.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Examples

Shows how to split document by pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### See Also

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
