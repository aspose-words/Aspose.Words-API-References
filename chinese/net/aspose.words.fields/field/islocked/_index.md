---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words for .NET
description: 探索字段的 IsLocked 属性——控制重新计算并增强数据完整性。立即解锁高效的数据结果管理！
type: docs
weight: 50
url: /zh/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

获取或设置字段是否被锁定（不应重新计算其结果）。

```csharp
public bool IsLocked { get; set; }
```

## 例子

展示如何使用 FieldStart 节点。

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

// 检索代表文档中的字段的外观对象。
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// 更新字段以显示当前日期。
field.Update();
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
