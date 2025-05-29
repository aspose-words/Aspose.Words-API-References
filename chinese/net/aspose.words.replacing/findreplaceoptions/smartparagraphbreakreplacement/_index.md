---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words for .NET
description: 在 FindReplaceOptions 中探索 SmartParagraphBreakReplacement 属性。轻松控制段落分隔符，实现无缝文本格式化。
type: docs
weight: 170
url: /zh/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

获取或设置一个布尔值，指示当没有下一个同级段落时是否允许替换段落 break 。

默认值为`错误的`。

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## 评论

此选项允许在没有下一个同级段落可将所有 child 节点移动到该段落时，通过查找被替换段落之后的任何下一个段落（不一定是同级段落）来替换段落中断。

## 例子

展示如何从带有嵌套表格的表格单元格中删除段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在第一个单元格中创建带有段落和内部表格的表格。
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// 当以下选项设置为“true”时，Aspose.Words 将删除段落的文本
// 完全与段落标记一致。否则，Aspose.Words 将模仿 Word 并删除
// 仅段落的文本并保留段落标记（当表格跟在文本后面时）。
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
