---
title: Field.Type
second_title: Aspose.Words for .NET API 参考
description: Field 财产. 获取 Microsoft Word 字段类型
type: docs
weight: 100
url: /zh/net/aspose.words.fields/field/type/
---
## Field.Type property

获取 Microsoft Word 字段类型。

```csharp
public virtual FieldType Type { get; }
```

### 例子

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

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../field/)
* 部件 [Aspose.Words](../../../)


