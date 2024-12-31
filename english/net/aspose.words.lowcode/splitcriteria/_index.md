---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.SplitCriteria enum. Specifies how the document is split into parts in C#.
type: docs
weight: 4270
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

Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", new SplitOptions() { SplitCriteria = SplitCriteria.Page });
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, new SplitOptions() { SplitCriteria = SplitCriteria.Page });
```

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
