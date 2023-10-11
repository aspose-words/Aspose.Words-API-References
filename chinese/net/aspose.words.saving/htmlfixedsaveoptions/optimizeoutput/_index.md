---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Aspose.Words for .NET API 参考
description: HtmlFixedSaveOptions 财产. 标志指示是否需要优化输出 如果设置此标志则冗余嵌套画布并删除空画布 还将连接具有相同格式的相邻字形 注意如果出现以下情况内容显示的准确性可能会受到影响该属性设置为真的. 默认为真的.
type: docs
weight: 100
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

标志指示是否需要优化输出。 如果设置此标志，则冗余嵌套画布并删除空画布， 还将连接具有相同格式的相邻字形。 注意：如果出现以下情况，内容显示的准确性可能会受到影响该属性设置为`真的`. 默认为`真的`.

```csharp
public override bool OptimizeOutput { get; set; }
```

### 例子

演示如何在将文档保存为 HTML 时通过删除各种冗余对象来简化文档。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// 优化版本的文档大小几乎是未优化文档大小的三分之一。
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* 部件 [Aspose.Words](../../../)


