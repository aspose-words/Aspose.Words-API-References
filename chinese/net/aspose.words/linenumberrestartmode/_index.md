---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words for .NET
description: 发现 Aspose.Words.LineNumberRestartMode 枚举来控制自动行号重置，以增强文档格式和清晰度。
type: docs
weight: 3880
url: /zh/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

确定自动行号何时重新开始。

```csharp
public enum LineNumberRestartMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| RestartPage | `0` | 行号从每一页的开头重新开始。 |
| RestartSection | `1` | 行号从章节开始处重新开始。 |
| Continuous | `2` | 行号与上一节连续。 |

## 例子

展示如何为某个部分启用行号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以使用该部分的 PageSetup 对象在该部分文本行的左侧显示数字。
// 这与 List 对象的行为相同，
// 但它覆盖了整个部分并且不以任何方式修改文本。
// 我们的部分将在每个新页面上从 1 重新开始编号并显示数字，
// 如果它是 3 的倍数，则位于行左侧 50pt 处。
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// 行计数器将跳过任何将“SuppressLineNumbers”标志设置为“true”的段落。
// 本段位于第 15 行，是 3 的倍数，因此通常会显示行号。
// 该部分的行计数器也会忽略这一行，将下一行视为第 15 行，
//并从该点继续计数。
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### 也可以看看

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
