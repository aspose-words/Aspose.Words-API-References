---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words for .NET
description: 探索 ParagraphFormat 的 NoSpaceBetweenParagraphsOfSameStyle 属性。通过消除相同样式段落之间的空格来优化文档布局。
type: docs
weight: 250
url: /zh/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

当`真的`，[`SpaceBefore`](../spacebefore/)和[`SpaceAfter`](../spaceafter/)将被忽略 相同样式的段落之间。

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## 评论

此设置仅应用于段落样式时才会生效。如果直接应用于段落，则无效。

## 例子

展示如何在相同样式的段落之间不应用间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在该构建器将创建的段落前后应用大量间距。
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// 将“NoSpaceBetweenParagraphsOfSameStyle”标志设置为“true”以应用
// 相同样式的段落之间没有间距，这会将相似的段落分组。
// 将“NoSpaceBetweenParagraphsOfSameStyle”标志保留为“false”
// 均匀地将间距应用于每个段落。
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
