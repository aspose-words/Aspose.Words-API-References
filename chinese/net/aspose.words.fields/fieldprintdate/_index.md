---
title: FieldPrintDate Class
linktitle: FieldPrintDate
articleTitle: FieldPrintDate
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldPrintDate 类，轻松实现 PRINTDATE 字段，增强文档自动化和效率。
type: docs
weight: 2700
url: /zh/net/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class

实现 PRINTDATE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldPrintDate : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldPrintDate](fieldprintdate/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseLunarCalendar](../../aspose.words.fields/fieldprintdate/uselunarcalendar/) { get; set; } | 获取或设置是否使用伊斯兰历或希伯来历。 |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldprintdate/usesakaeracalendar/) { get; set; } | 获取或设置是否使用萨迦历法。 |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldprintdate/useumalquracalendar/) { get; set; } | 获取或设置是否使用 Um-al-Qura 日历。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

检索文档上次打印的日期和时间。默认情况下，使用公历。

## 例子

显示已读 PRINTDATE 字段。

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// 当文档被打印机打印或打印为 PDF（但未导出为 PDF）时，
// PRINTDATE 字段将显示打印操作的日期/时间。
// 如果没有进行打印，这些字段将显示“0/0/0000”。
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// 下面是三种不同的日历类型，PRINTDATE 字段根据
// 可以显示上次打印操作的日期和时间。
// 1 - 伊斯兰阴历：
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - 古兰经日历：
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - 印度国家日历：
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
