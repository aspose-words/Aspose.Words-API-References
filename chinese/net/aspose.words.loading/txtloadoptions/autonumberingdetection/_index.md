---
title: TxtLoadOptions.AutoNumberingDetection
second_title: Aspose.Words for .NET API 参考
description: TxtLoadOptions 财产. 获取或设置一个布尔值指示加载文档时是否执行自动编号检测  默认值为真的.
type: docs
weight: 20
url: /zh/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

获取或设置一个布尔值，指示加载文档时是否执行自动编号检测 。 默认值为`真的`.

```csharp
public bool AutoNumberingDetection { get; set; }
```

### 例子

演示如何禁用自动编号检测。

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### 也可以看看

* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../txtloadoptions/)
* 部件 [Aspose.Words](../../../)


