---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.NumSpacing 枚举，自定义数字间距，增强文档格式。立即提升您的文本呈现效果！
type: docs
weight: 5030
url: /zh/net/aspose.words/numspacing/
---
## NumSpacing enumeration

指定可以显示数字间距的可能值。

```csharp
public enum NumSpacing
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Default | `0` | 指定以字体的默认形式显示数字。 |
| Proportional | `1` | 指定如果字体支持，则显示按比例间隔设计的数字形式。 |
| Tabular | `2` | 指定如果字体支持，则显示表格形式的数字。 |

## 例子

展示如何设置数字的间距类型。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 此效果仅在较新版本的 MS Word 中受支持。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
