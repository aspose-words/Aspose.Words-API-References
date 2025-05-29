---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words for .NET
description: 使用 FixedPageSaveOptions 的 OptimizeOutput 属性增强文档输出。删除冗余内容并优化格式，以获得更清晰的显示效果。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

标志指示是否需要优化输出。 如果设置了此标志，则会删除多余的嵌套画布和空画布， 还会连接具有相同格式的相邻字形。 注意：如果将此属性设置为`真的`. 默认为`错误的`.

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## 例子

显示如何在保存为 xps 时优化文档对象。

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// 创建一个“XpsSaveOptions”对象传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions saveOptions = new XpsSaveOptions();
// 将“OptimizeOutput”属性设置为“true”以采取措施，例如删除嵌套或空画布
// 并连接具有相同格式的相邻运行以优化输出文档的内容。
// 这可能会影响文档的外观。
// 将“OptimizeOutput”属性设置为“false”以正常保存文档。
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### 也可以看看

* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
