---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words for .NET
description: 使用 HtmlFixedSaveOptions 属性优化您的 HTML 输出。通过移除冗余画布并合并相似的字形来提升性能。默认值为 true。
type: docs
weight: 110
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

标志指示是否需要优化输出。 如果设置了此标志，则会删除多余的嵌套画布和空画布， 还会连接具有相同格式的相邻字形。 注意：如果将此属性设置为`真的`. 默认为`真的`.

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
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
