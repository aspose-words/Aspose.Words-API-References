---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: SplitOptions SplitCriteria property. Specifies the criteria for splitting the document into parts in C#.
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

Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", new SplitOptions() { SplitCriteria = SplitCriteria.Page });
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, new SplitOptions() { SplitCriteria = SplitCriteria.Page });
```

### See Also

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
