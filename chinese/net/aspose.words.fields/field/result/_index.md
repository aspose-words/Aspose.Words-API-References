---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: 用于 .NET 的 Aspose.Words
description: Field Result 财产. 获取或设置字段分隔符和字段结束之间的文本 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.fields/field/result/
---
## Field.Result property

获取或设置字段分隔符和字段结束之间的文本。

```csharp
public string Result { get; set; }
```

## 例子

演示如何使用域代码将域插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的此重载会自动更新插入的字段。
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
