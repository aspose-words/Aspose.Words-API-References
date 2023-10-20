---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.LineNumberRestartMode 枚举. 确定自动行编号何时重新启动 在 C#.
type: docs
weight: 3430
url: /zh/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

确定自动行编号何时重新启动。

```csharp
public enum LineNumberRestartMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| RestartPage | `0` | 行编号在每页开头重新开始。 |
| RestartSection | `1` | 行编号在节开始处重新开始。 |
| Continuous | `2` | 与上一节连续的行编号。 |

## 例子

展示如何为节启用行编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以使用该部分的 PageSetup 对象在该部分的文本行左侧显示数字。
// 这与 List 对象的行为相同，
// 但它覆盖了整个部分并且不会以任何方式修改文本。
// 我们的部分将在每个新页面上从 1 重新开始编号并显示编号，
// 如果是 3 的倍数，则在该行左侧 50pt 处。
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// 行计数器将跳过“SuppressLineNumbers”标志设置为“true”的任何段落。
// 该段落位于第 15 行，该行是 3 的倍数，因此通常会显示行号。
// 该部分的行计数器也会忽略这一行，将下一行视为第 15 行，
// 并从该点开始继续计数。
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### 也可以看看

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
