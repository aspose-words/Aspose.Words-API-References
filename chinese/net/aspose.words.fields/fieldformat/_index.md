---
title: FieldFormat Class
linktitle: FieldFormat
articleTitle: FieldFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldFormat 类，轻松访问数字、日期和时间字段。使用强大的功能增强文档格式！
type: docs
weight: 2350
url: /zh/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

提供对字段的数字、日期和时间以及常规格式的类型访问。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat/) { get; set; } | 获取或设置应用于日期和时间字段结果的格式。对应于 \@ 开关。 |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats/) { get; } | 获取应用于数字、文本或任何字段结果的通用格式集合。 对应于 \* 开关。 |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat/) { get; set; } | 获取或设置应用于数值字段结果的格式。对应于 \# 开关。 |

## 例子

显示如何格式化字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入一个显示未应用格式的结果的字段。
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// 我们可以使用字段的属性将格式应用于字段的结果。
// 以下是我们可以应用于字段结果的三种格式。
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

// 我们可以删除格式以将字段的结果恢复为其原始形式。
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
