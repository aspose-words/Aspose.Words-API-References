---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: 轻松管理字段结果属性。访问或修改字段分隔符之间的文本，简化数据处理并提高效率。
type: docs
weight: 70
url: /zh/net/aspose.words.fields/field/result/
---
## Field.Result property

获取或设置字段分隔符和字段结尾之间的文本。

```csharp
public string Result { get; set; }
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

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
