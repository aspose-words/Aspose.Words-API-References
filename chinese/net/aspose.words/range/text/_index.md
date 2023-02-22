---
title: Range.Text
second_title: Aspose.Words for .NET API 参考
description: Range 财产. 获取范围的文本
type: docs
weight: 50
url: /zh/net/aspose.words/range/text/
---
## Range.Text property

获取范围的文本。

```csharp
public string Text { get; }
```

### 评论

返回的字符串包括所有控制和特殊字符，如[`ControlChar`](../../controlchar/).

### 例子

显示如何获取范围涵盖的所有节点的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### 也可以看看

* class [Range](../)
* 命名空间 [Aspose.Words](../../range/)
* 部件 [Aspose.Words](../../../)


