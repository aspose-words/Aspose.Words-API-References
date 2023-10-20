---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: 用于 .NET 的 Aspose.Words
description: FieldChar FieldType 财产. 返回字段的类型 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

返回字段的类型。

```csharp
public FieldType FieldType { get; }
```

## 例子

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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
