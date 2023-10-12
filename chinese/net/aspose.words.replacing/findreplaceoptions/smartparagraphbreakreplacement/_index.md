---
title: FindReplaceOptions.SmartParagraphBreakReplacement
second_title: Aspose.Words for .NET API 参考
description: FindReplaceOptions 财产. 获取或设置一个布尔值指示当没有下一个兄弟段落时是否允许替换段落break 
type: docs
weight: 160
url: /zh/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

获取或设置一个布尔值，指示当没有下一个兄弟段落时是否允许替换段落break 。

默认值为`错误的`。

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

### 评论

当没有所有 child 节点可以移动到的下一个兄弟段落时，此选项允许通过在被替换的段落后查找任何（不一定是兄弟）下一个段落来替换段落分隔符。

### 例子

演示如何从具有嵌套表格的表格单元格中删除段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在第一个单元格中创建包含段落和内部表格的表格。
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
// 完全带有段落标记。否则，Aspose.Words 将模仿 Word 并删除
// 仅段落文本并保持段落标记不变（当文本后面有表格时）。
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../findreplaceoptions/)
* 部件 [Aspose.Words](../../../)


