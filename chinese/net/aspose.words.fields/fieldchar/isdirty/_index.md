---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: 用于 .NET 的 Aspose.Words
description: FieldChar IsDirty 财产. 获取或设置字段的当前结果是否由于对文档进行的其他修改 而不再正确陈旧 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

获取或设置字段的当前结果是否由于对文档进行的其他修改 而不再正确（陈旧）。

```csharp
public bool IsDirty { get; set; }
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

* class [FieldChar](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
