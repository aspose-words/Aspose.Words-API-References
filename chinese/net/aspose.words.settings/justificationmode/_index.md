---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words JustificationMode 枚举，用于精确调整文档中的字符间距。通过可自定义的设置增强可读性！
type: docs
weight: 6630
url: /zh/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

指定文档的字符间距调整。 默认值为`扩张`.

```csharp
public enum JustificationMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Expand | `0` | 不压缩字符间距。 |
| Compress | `1` | 压缩字符间距。 |
| CompressKana | `2` | 压缩，使用假名音节表、平假名和片假名的规则。 |

## 例子

展示如何管理字符间距控制。

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
