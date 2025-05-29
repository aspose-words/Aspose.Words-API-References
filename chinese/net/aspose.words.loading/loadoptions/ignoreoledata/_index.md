---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: Aspose.Words for .NET
description: 了解 LoadOptions IgnoreOleData 属性如何通过控制 OLE 数据处理来增强数据处理能力。立即优化您的工作流程！
type: docs
weight: 70
url: /zh/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

指定是否忽略 OLE 数据。

```csharp
public bool IgnoreOleData { get; set; }
```

## 评论

忽略 OLE 数据可能会减少内存消耗并提高性能，并且在目标格式不支持 OLE 对象的情况下不会丢失数据。

默认值为`错误的`。

## 例子

显示如何在加载时忽略 OLE 数据。

```csharp
// 忽略 OLE 数据可能会减少内存消耗并提高性能
// 当目标格式不支持 OLE 对象时，不会丢失数据。
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
