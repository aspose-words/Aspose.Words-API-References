---
title: Field.LocaleId
second_title: Aspose.Words for .NET API 参考
description: Field 财产. 获取或设置字段的 LCID
type: docs
weight: 60
url: /zh/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

获取或设置字段的 LCID。

```csharp
public int LocaleId { get; set; }
```

### 例子

演示如何插入字段并使用其区域设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个日期字段，然后打印它将显示的日期。
// 您线程的当前区域性决定了日期的格式。
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// 更改线程的区域性将影响 DATE 字段的结果。
// 让 DATE 字段以不同区域性显示日期的另一种方法是使用其 LocaleId 属性。
// 这种方式允许我们避免改变线程的区域性来获得这种效果。
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../field/)
* 部件 [Aspose.Words](../../../)


