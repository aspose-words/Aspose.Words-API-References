---
title: FieldDate Class
linktitle: FieldDate
articleTitle: FieldDate
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldDate 类，旨在轻松实现 DATE 字段，增强文档自动化和格式化。
type: docs
weight: 2180
url: /zh/net/aspose.words.fields/fielddate/
---
## FieldDate class

实现 DATE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldDate : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldDate](fielddate/)() | 默认构造函数。 |

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
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat/) { get; set; } | 获取或设置插入新的 DATE 字段时是否使用托管应用程序上次使用的格式。 |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar/) { get; set; } | 获取或设置是否使用伊斯兰历或希伯来历。 |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar/) { get; set; } | 获取或设置是否使用萨迦历法。 |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar/) { get; set; } | 获取或设置是否使用 Um-al-Qura 日历。 |

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

插入当前日期和时间。默认使用公历。

## 例子

展示如何使用 DATE 字段根据不同类型的日历显示日期。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们希望文档中的文本始终显示正确的日期，我们可以使用 DATE 字段。
// 以下是 DATE 字段可以用来显示日期的三种文化日历。
// 1 - 伊斯兰阴历：
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - 古兰经日历：
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - 印度国家日历：
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// 插入一个 DATE 字段并将其日历类型设置为主机应用程序最后使用的日历类型。
// 在 Microsoft Word 中，类型将是插入 -> 文本 -> 日期和时间对话框中最近使用的类型。
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
