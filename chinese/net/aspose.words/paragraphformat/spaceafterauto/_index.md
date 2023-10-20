---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat SpaceAfterAuto 财产. 如果自动设置段落后的间距量则为真 在 C#.
type: docs
weight: 310
url: /zh/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

如果自动设置段落后的间距量，则为真。

```csharp
public bool SpaceAfterAuto { get; set; }
```

## 评论

当设置为 true 时，覆盖[`SpaceAfter`](../spaceafter/).

当您将段落之前和之后的空间设置为自动时， Microsoft Word 根据以下规则自动在段落之间添加 14 点间距 ：

* 通常，在所有段落之后添加间距。
* 在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。 列表项之间不添加间距。
* 在嵌套的项目符号或编号列表中，不添加间距。
* 间距通常在表格之后添加。
* 如果表格是表格单元格中的最后一个块，则不会在表格之后添加间距。
* 在表格单元格的最后一段之后不添加间距。

## 例子

显示如何设置自动段落间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在此构建器将创建的段落之前和之后应用大量间距。
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// 将这些标志设置为“true”以应用自动间距，
// 有效地忽略了我们在上面设置的属性中的间距。
// 将它们保留为“false”将应用我们的自定义段落间距。
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// 插入两个在其上方和下方有间距的段落并保存文档。
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
