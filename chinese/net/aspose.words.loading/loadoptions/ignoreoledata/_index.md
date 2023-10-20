---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: 用于 .NET 的 Aspose.Words
description: LoadOptions IgnoreOleData 财产. 指定是否忽略 OLE 数据 在 C#.
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

当目标格式不支持 OLE 对象时，忽略 OLE 数据可以减少内存消耗并提高性能，而不会丢失数据。

默认值为`错误的`。

## 例子

演示如何在加载时忽略 OLE 数据。

```csharp
// 忽略OLE数据可能会减少内存消耗并提高性能
// 当目标格式不支持 OLE 对象时不会丢失数据。
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
