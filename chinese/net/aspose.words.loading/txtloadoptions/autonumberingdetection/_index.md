---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words for .NET
description: 探索 TxtLoadOptions 的 AutoNumberingDetection 属性。轻松启用或禁用自动编号，实现无缝文档加载。默认值为 true。
type: docs
weight: 20
url: /zh/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

获取或设置一个布尔值，指示在加载文档时是否执行自动编号检测。 默认值为`真的`.

```csharp
public bool AutoNumberingDetection { get; set; }
```

## 例子

展示如何禁用自动编号检测。

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### 也可以看看

* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
