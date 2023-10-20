---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.GeneralFormatCollection 班级. 表示一般格式的类型化集合 在 C#.
type: docs
weight: 2650
url: /zh/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

表示一般格式的类型化集合。

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | 获取集合中的项目总数。 |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | 获取指定索引处的通用格式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | 向集合添加通用格式。 |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | 返回一个枚举器对象。 |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | 从集合中删除所有出现的指定通用格式。 |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | 删除指定索引处出现的一般格式。 |

## 例子

显示如何格式化字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档构建器插入一个显示未应用格式的结果的字段。
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// 我们可以使用字段的属性将格式应用于字段的结果。
// 下面是我们可以应用于字段结果的三种格式。
// 1 - 数字格式：
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - 日期/时间格式：
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - 一般格式：
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// 我们可以删除格式以将字段的结果恢复为原始形式。
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### 也可以看看

* enum [GeneralFormat](../generalformat/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
