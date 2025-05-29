---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Comparing.Granularity 枚举，轻松精准地追踪文档变更。立即增强您的文档比较功能！
type: docs
weight: 490
url: /zh/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

指定比较两个文档时要跟踪的更改的粒度。

```csharp
public enum Granularity
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| CharLevel | `0` | 指定字符级别的更改。 |
| WordLevel | `1` | 指定单词级别的更改。 |

## 例子

显示在比较文档时指定粒度。

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// 指定是否跟踪更改
// 按字符（'Granularity.CharLevel'）或按单词（'Granularity.WordLevel'）。
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// 第一个文档的修订组集合包含文档之间的所有差异。
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Comparing](../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../)
