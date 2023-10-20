---
title: ParagraphFormat.SpaceBefore
linktitle: SpaceBefore
articleTitle: SpaceBefore
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat SpaceBefore 财产. 获取或设置段落之前的间距以磅为单位 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

获取或设置段落之前的间距（以磅为单位）。

```csharp
public double SpaceBefore { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

## 评论

当[`SpaceBeforeAuto`](../spacebeforeauto/)是`真的`。

有效值范围为 0 到 1584（包含 0 和 1584）。

## 例子

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

演示如何在具有相同样式的段落之间应用无间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在该构建器将创建的段落之前和之后应用大量间距。
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// 将“NoSpaceBetweenParagraphsOfSameStyle”标志设置为“true”以应用
// 相同样式的段落之间没有间距，这会将相似的段落分组。
// 将“NoSpaceBetweenParagraphsOfSameStyle”标志保留为“false”
// 对每个段落均匀应用间距。
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
