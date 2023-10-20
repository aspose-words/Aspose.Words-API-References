---
title: BuildVersionInfo Class
linktitle: BuildVersionInfo
articleTitle: BuildVersionInfo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.BuildVersionInfo 班级. 提供有关当前产品名称和版本的信息 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/buildversioninfo/
---
## BuildVersionInfo class

提供有关当前产品名称和版本的信息。

要了解更多信息，请访问[输出文档中包含的生成者或生产者名称](https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/)文档文章。

```csharp
public static class BuildVersionInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [Product](../../aspose.words/buildversioninfo/product/) { get; } | 获取产品的全名。 |
| static [Version](../../aspose.words/buildversioninfo/version/) { get; } | 获取产品版本。 |

## 例子

演示如何显示有关已安装的 Aspose.Words 版本的信息。

```csharp
Console.WriteLine($"I am currently using {BuildVersionInfo.Product}, version number {BuildVersionInfo.Version}!");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
