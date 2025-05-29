---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words for .NET
description: 探索 CompareOptions Granularity 属性，按字符或单词跟踪更改，实现精准的文本编辑。立即增强您的文档控制！
type: docs
weight: 40
url: /zh/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

指定是否按字符或按字跟踪更改。

```csharp
public Granularity Granularity { get; set; }
```

## 评论

默认值为WordLevel.

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../../)
