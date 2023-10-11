---
title: Enum JustificationMode
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Settings.JustificationMode 枚举. 指定文档的字符间距调整 默认值为扩张.
type: docs
weight: 5800
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
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

### 例子

演示如何管理字符间距控制。

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


