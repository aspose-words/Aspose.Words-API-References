---
title: PageSetup.LineNumberDistanceFromText
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置行号右边缘与文档左边缘之间的距离
type: docs
weight: 220
url: /zh/net/aspose.words/pagesetup/linenumberdistancefromtext/
---
## PageSetup.LineNumberDistanceFromText property

获取或设置行号右边缘与文档左边缘之间的距离。

```csharp
public double LineNumberDistanceFromText { get; set; }
```

### 评论

将此属性设置为零，以实现文档行号和文本之间的自动距离。

### 例子

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

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


