---
title: CompareOptions.Granularity
second_title: Aspose.Words for .NET API 参考
description: CompareOptions 财产. 指定是按字符还是按单词跟踪更改 默认值为WordLevel.
type: docs
weight: 20
url: /zh/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

指定是按字符还是按单词跟踪更改。 默认值为WordLevel.

```csharp
public Granularity Granularity { get; set; }
```

### 例子

显示以在比较文档时指定粒度。

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// 指定是否跟踪变化
// 按字符 ('Granularity.CharLevel')，或按单词 ('Granularity.WordLevel')。
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// 第一个文档的修订组集合包含文档之间的所有差异。
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### 也可以看看

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../compareoptions/)
* 部件 [Aspose.Words](../../../)


