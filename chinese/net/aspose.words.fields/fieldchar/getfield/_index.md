---
title: FieldChar.GetField
second_title: Aspose.Words for .NET API 参考
description: FieldChar 方法. 为字段 char 返回一个字段
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

为字段 char 返回一个字段。

```csharp
public Field GetField()
```

### 返回值

字段 char 的字段。

### 评论

一个新的[`Field`](../../field/)每次调用该方法时都会创建对象。

### 例子

显示如何使用 FieldStart 节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// 检索代表文档中字段的外观对象。
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// 更新字段以显示当前日期。
field.Update();
```

### 也可以看看

* class [Field](../../field/)
* class [FieldChar](../)
* 命名空间 [Aspose.Words.Fields](../../fieldchar/)
* 部件 [Aspose.Words](../../../)


