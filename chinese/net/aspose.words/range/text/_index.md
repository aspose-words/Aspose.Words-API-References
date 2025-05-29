---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 发现范围文本属性，轻松检索和操作指定范围内的文本，以增强内容管理。
type: docs
weight: 60
url: /zh/net/aspose.words/range/text/
---
## Range.Text property

获取范围的文本。

```csharp
public string Text { get; }
```

## 评论

返回的字符串包括所有控制字符和特殊字符，如中所述[`ControlChar`](../../controlchar/)。

## 例子

展示如何获取某个范围覆盖的所有节点的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### 也可以看看

* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
