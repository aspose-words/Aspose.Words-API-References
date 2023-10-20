---
title: FieldCreateDate Class
linktitle: FieldCreateDate
articleTitle: FieldCreateDate
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldCreateDate 班级. 实现 CREATEDATE 字段 在 C#.
type: docs
weight: 1720
url: /zh/net/aspose.words.fields/fieldcreatedate/
---
## FieldCreateDate class

实现 CREATEDATE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldCreateDate : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldCreateDate](fieldcreatedate/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseLunarCalendar](../../aspose.words.fields/fieldcreatedate/uselunarcalendar/) { get; set; } | 获取或设置是否使用回历农历或希伯来农历。 |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldcreatedate/usesakaeracalendar/) { get; set; } | 获取或设置是否使用Saka Era日历。 |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldcreatedate/useumalquracalendar/) { get; set; } | 获取或设置是否使用 Um-al-Qura 日历。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

## 评论

检索文档的创建日期和时间。默认使用公历。

## 例子

演示如何使用 CREATEDATE 字段来显示文档的创建日期/时间。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// 我们可以使用 CREATEDATE 字段来显示文档的创建日期和时间。
// 下面是三种不同的日历类型，CREATEDATE 字段可以根据它们显示日期/时间。
// 1 - 伊斯兰农历：
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - 乌姆古拉历：
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - 印度国家日历：
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
