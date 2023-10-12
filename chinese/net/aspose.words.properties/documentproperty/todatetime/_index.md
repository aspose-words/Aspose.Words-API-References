---
title: DocumentProperty.ToDateTime
second_title: Aspose.Words for .NET API 参考
description: DocumentProperty 方法. 将属性值返回为 约会时间以 UTC 时间表示
type: docs
weight: 80
url: /zh/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

将属性值返回为 **约会时间**以 UTC 时间表示。

```csharp
public DateTime ToDateTime()
```

### 评论

如果属性类型不是，则抛出异常DateTime。

Microsoft Word 仅存储自定义日期属性的日期部分（无时间）。

### 例子

演示如何创建包含日期和时间的自定义文档属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

显示自定义文档属性的各种类型转换方法。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### 也可以看看

* class [DocumentProperty](../)
* 命名空间 [Aspose.Words.Properties](../../documentproperty/)
* 部件 [Aspose.Words](../../../)


