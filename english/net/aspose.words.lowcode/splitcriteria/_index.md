---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.LowCode.SplitCriteria enum for efficient document splitting. Optimize your workflow with versatile options for seamless part management.
type: docs
weight: 4390
url: /net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Specifies how the document is split into parts.

```csharp
public enum SplitCriteria
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Page | `0` | Specifies that the document is split into pages. |
| SectionBreak | `1` | Specifies that the document is split into parts at a section break of any type. |
| Style | `2` | Specifies that the document is split into parts at a paragraph formatted using the style specified in [`SplitStyle`](../splitoptions/splitstyle/). |

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

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
