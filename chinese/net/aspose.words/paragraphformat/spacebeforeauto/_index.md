---
title: ParagraphFormat.SpaceBeforeAuto
linktitle: SpaceBeforeAuto
articleTitle: SpaceBeforeAuto
second_title: Aspose.Words for .NET
description: 探索 ParagraphFormat SpaceBeforeAuto 属性。自动调整段落间距，让您的文档呈现更美观、更专业的外观。
type: docs
weight: 340
url: /zh/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

如果段落前的间距量是自动设置的，则为真。

```csharp
public bool SpaceBeforeAuto { get; set; }
```

## 评论

当设置为`真的`，覆盖了[`SpaceBefore`](../spacebefore/)。

当您将段落前间距和段落后间距设置为“自动”时，Microsoft Word 会根据以下规则自动在段落之间添加 14 磅的间距：

* 通常，所有段落后都会添加间距。
* 在项目符号列表或编号列表中，仅在列表的最后一项后添加间距。 列表项之间不添加间距。
* 在嵌套的项目符号列表或编号列表中不添加间距。
* 通常在表格后添加空格。
* 如果表格是表格单元格中的最后一个块，则不会在表格后添加间距。
* 表格单元格中最后一段之后未添加间距。

## 例子

显示如何设置自动段落间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在该构建器将创建的段落前后应用大量间距。
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// 将这些标志设置为“true”以应用自动间距，
// 有效地忽略了我们上面设置的属性中的间距。
// 将它们保留为“false”将应用我们的自定义段落间距。
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// 插入两个上下有间距的段落并保存文档。
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
