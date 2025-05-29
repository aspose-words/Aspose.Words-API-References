---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words for .NET
description: 探索 LayoutOptions 的 CommentDisplayMode 属性，自定义评论渲染。轻松设置，使用 ShowInBalloons 等选项提升用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

获取或设置评论的呈现方式。 默认值为ShowInBalloons.

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## 评论

请注意，修订不会在气球中呈现ShowInAnnotations.

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

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
