---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 使用我们的“字段类型”属性探索 Microsoft Word 字段类型。使用精确的格式和动态内容功能增强您的文档。
type: docs
weight: 100
url: /zh/net/aspose.words.fields/field/type/
---
## Field.Type property

获取 Microsoft Word 字段类型。

```csharp
public virtual FieldType Type { get; }
```

## 例子

展示如何使用字段代码将字段插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的此重载会自动更新插入的字段。
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### 也可以看看

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
