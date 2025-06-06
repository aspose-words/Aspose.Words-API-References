---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.CommentDisplayMode 枚举，优化文档注释的渲染。立即提升文档的清晰度和呈现效果！
type: docs
weight: 3740
url: /zh/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

指定文档注释的渲染模式。

```csharp
public enum CommentDisplayMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Hide | `0` | 没有呈现文档注释。 |
| ShowInBalloons | `1` | 将文档注释显示在页边空白处的气泡框中。这是默认值。 |
| ShowInAnnotations | `2` | 在注释中显示文档评论。此功能仅适用于 PDF 格式。 |

## 例子

展示如何在将文档保存为渲染格式时显示注释。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations 仅适用于 Pdf1.7 和 Pdf1.5 格式。
// 在其他格式中，它的工作方式与隐藏类似。
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// 请注意，需要重建文档页面布局（通过 Document.UpdatePageLayout() 方法）
// 更改 Document.LayoutOptions 值之后。
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
