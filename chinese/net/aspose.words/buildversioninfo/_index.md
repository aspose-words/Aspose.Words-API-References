---
title: BuildVersionInfo Class
linktitle: BuildVersionInfo
articleTitle: BuildVersionInfo
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.BuildVersionInfo 类，获取有关产品名称和版本的详细信息。使用可靠的数据增强您的文档管理！
type: docs
weight: 310
url: /zh/net/aspose.words/buildversioninfo/
---
## BuildVersionInfo class

提供有关当前产品名称和版本的信息。

要了解更多信息，请访问[输出文档中包含的生成器或生产者名称](https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/)文档文章。

```csharp
public static class BuildVersionInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [Product](../../aspose.words/buildversioninfo/product/) { get; } | 获取产品的全名。 |
| static [Version](../../aspose.words/buildversioninfo/version/) { get; } | 获取产品版本。 |

## 例子

展示如何显示有关您安装的 Aspose.Words 版本的信息。

```csharp
Console.WriteLine($"I am currently using {BuildVersionInfo.Product}, version number {BuildVersionInfo.Version}!");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
