---
title: OptimizeOutput
second_title: Aspose.Words for .NET API 参考
description: 标志表示是否需要优化输出 如果设置了这个标志多余的嵌套画布和空的画布被删除 也会连接具有相同格式的相邻字形 注意内容显示的准确性可能会受到影响如果此属性设置为 true 默认为 false
type: docs
weight: 50
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

标志表示是否需要优化输出。 如果设置了这个标志，多余的嵌套画布和空的画布被删除， 也会连接具有相同格式的相邻字形。 注意：内容显示的准确性可能会受到影响，如果此属性设置为 true。 默认为 false。

```csharp
public virtual bool OptimizeOutput { get; set; }
```

### 例子

显示如何在保存到 xps 时优化文档对象。

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// 创建一个“XpsSaveOptions”对象以传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .XPS。
XpsSaveOptions saveOptions = new XpsSaveOptions();

// 将“OptimizeOutput”属性设置为“true”，采取移除嵌套或空画布等措施
// 并连接具有相同格式的相邻运行以优化输出文档的内容。
// 这可能会影响文档的外观。
// 将“OptimizeOutput”属性设置为“false”以正常保存文档。
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### 也可以看看

* class [FixedPageSaveOptions](../../fixedpagesaveoptions)
* 命名空间 [Aspose.Words.Saving](../../fixedpagesaveoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->