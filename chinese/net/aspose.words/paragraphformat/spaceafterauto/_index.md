---
title: ParagraphFormat.SpaceAfterAuto
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 如果自动设置段落后的间距则为 True
type: docs
weight: 310
url: /zh/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

如果自动设置段落后的间距，则为 True。

```csharp
public bool SpaceAfterAuto { get; set; }
```

### 评论

当设置为`真的`，覆盖效果[`SpaceAfter`](../spaceafter/)。

当您将段落前间距和后间距设置为自动时， Microsoft Word 根据以下规则自动在段落之间添加 14 磅间距 ：

* 通常，所有段落后都会添加间距。
* 在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。 列表项之间不添加间距。
* 在嵌套的项目符号列表或编号列表中，不添加间距。
* 空格通常添加在表格之后。
* 如果表格是表格单元格中的最后一个块，则不会在表格后面添加间距。
* 表格单元格中最后一段之后不添加间距。

### 例子

演示如何设置自动段落间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在该构建器将创建的段落之前和之后应用大量间距。
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// 将这些标志设置为“true”以应用自动间距，
// 实际上忽略了我们上面设置的属性中的间距。
// 将它们保留为“false”将应用我们的自定义段落间距。
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// 插入两个段落，上下有间距并保存文档。
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


