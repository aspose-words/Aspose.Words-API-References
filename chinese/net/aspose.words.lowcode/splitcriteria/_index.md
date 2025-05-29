---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LowCode.SplitCriteria 枚举，实现高效的文档拆分。使用多种选项优化您的工作流程，实现无缝文档管理。
type: docs
weight: 4400
url: /zh/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

指定如何将文档拆分成多个部分。

```csharp
public enum SplitCriteria
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Page | `0` | 指定将文档拆分为页面。 |
| SectionBreak | `1` | 指定文档在任意类型的分节符处拆分为多个部分。 |
| Style | `2` | 指定文档按段落拆分为多个部分，并使用[`SplitStyle`](../splitoptions/splitstyle/). |

## 例子

显示如何按页面拆分文档。

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### 也可以看看

* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
