---
title: PageSetup.LineStartingNumber
linktitle: LineStartingNumber
articleTitle: LineStartingNumber
second_title: Aspose.Words for .NET
description: 了解如何使用 PageSetup LineStartingNumber 属性轻松自定义文档的起始行号以增强格式。
type: docs
weight: 250
url: /zh/net/aspose.words/pagesetup/linestartingnumber/
---
## PageSetup.LineStartingNumber property

获取或设置起始行号。

```csharp
public int LineStartingNumber { get; set; }
```

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

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
