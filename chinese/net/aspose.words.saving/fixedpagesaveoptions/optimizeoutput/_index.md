---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: 用于 .NET 的 Aspose.Words
description: FixedPageSaveOptions OptimizeOutput 财产. 标志指示是否需要优化输出 如果设置此标志则冗余嵌套画布并删除空画布 还将连接具有相同格式的相邻字形 注意如果出现以下情况内容显示的准确性可能会受到影响该属性设置为真的. 默认为错误的 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

标志指示是否需要优化输出。 如果设置此标志，则冗余嵌套画布并删除空画布， 还将连接具有相同格式的相邻字形。 注意：如果出现以下情况，内容显示的准确性可能会受到影响该属性设置为`真的`. 默认为`错误的`.

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## 例子

演示如何在保存到 xps 时优化文档对象。

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// 创建一个“XpsSaveOptions”对象以传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions saveOptions = new XpsSaveOptions();

// 将“OptimizeOutput”属性设置为“true”以采取删除嵌套或空画布等措施
// 并用相同的格式连接相邻的运行以优化输出文档的内容。
// 这可能会影响文档的外观。
// 将“OptimizeOutput”属性设置为“false”以正常保存文档。
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### 也可以看看

* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
