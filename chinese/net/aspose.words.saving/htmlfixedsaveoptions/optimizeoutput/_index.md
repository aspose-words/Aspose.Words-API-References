---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions OptimizeOutput 财产. 标志表示是否需要优化输出 如果设置了这个标志多余的嵌套画布和空的画布被删除 也会连接具有相同格式的相邻字形 注意内容显示的准确性可能会受到影响如果此属性设置为 true 默认为 true 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

标志表示是否需要优化输出。 如果设置了这个标志，多余的嵌套画布和空的画布被删除， 也会连接具有相同格式的相邻字形。 注意：内容显示的准确性可能会受到影响，如果此属性设置为 true。 默认为 true。

```csharp
public override bool OptimizeOutput { get; set; }
```

## 例子

展示如何在将文档保存为 HTML 时通过删除各种冗余对象来简化文档。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// 优化后的文档大小几乎是未优化文档大小的三分之一。
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
