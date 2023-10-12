---
title: Range.UpdateFields
second_title: Aspose.Words for .NET API 参考
description: Range 方法. 更新此范围内文档字段的值
type: docs
weight: 120
url: /zh/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

更新此范围内文档字段的值。

```csharp
public void UpdateFields()
```

### 评论

当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，而是保持它们不变。 因此，如果您以编程方式修改了文档 并希望确保在保存之前调用此方法，则通常需要调用此方法正确的（计算出的）字段值出现在保存的文档中。

执行邮件合并后无需更新字段，因为邮件合并是一种字段 update 并自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关支持的字段类型的详细列表，请参阅程序员指南。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。 当您呈现文档或调用时，会更新与页面布局相关的字段[`UpdatePageLayout`](../../document/updatepagelayout/)。

要更新整个文档中的字段，请使用[`UpdateFields`](../../document/updatefields/)。

### 例子

展示如何更新某个范围内的所有字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// 上面的 DOCPROPERTY 字段将显示此内置文档属性的值。
doc.BuiltInDocumentProperties.Category = "MyCategory";

// 如果我们更新文档属性的值，我们将需要更新所有 DOCPROPERTY 字段才能显示它。
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// 更新第一部分范围内的所有字段。
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### 也可以看看

* class [Range](../)
* 命名空间 [Aspose.Words](../../range/)
* 部件 [Aspose.Words](../../../)


