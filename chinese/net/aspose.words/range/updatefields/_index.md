---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words for .NET
description: 使用 Range UpdateFields 方法轻松增强您的文档，快速有效地更新字段值以提高准确性。
type: docs
weight: 130
url: /zh/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

更新此范围内的文档字段的值。

```csharp
public void UpdateFields()
```

## 评论

当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，而是保持它们完好无损。 因此，如果您以编程方式修改了文档 并希望确保正确（计算）的字段值出现在保存的文档中，则通常需要在保存之前调用此方法。

执行邮件合并后无需更新字段，因为邮件合并是一种字段 update ，会自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关受支持的字段类型的详细列表，请参阅《程序员指南》。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。 当您呈现文档或调用时，页面布局相关的字段会更新[`UpdatePageLayout`](../../document/updatepagelayout/)。

要更新整个文档中的字段，请使用[`UpdateFields`](../../document/updatefields/)。

## 例子

显示如何更新某个范围内的所有字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// 上述 DOCPROPERTY 字段将显示此内置文档属性的值。
doc.BuiltInDocumentProperties.Category = "MyCategory";

// 如果我们更新文档属性的值，我们将需要更新所有 DOCPROPERTY 字段以显示它。
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// 更新第一部分范围内的所有字段。
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### 也可以看看

* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
