---
title: FieldMergeField Class
linktitle: FieldMergeField
articleTitle: FieldMergeField
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldMergeField 班级. 实现 MERGEFIELD 字段 在 C#.
type: docs
weight: 2150
url: /zh/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

实现 MERGEFIELD 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldMergeField : Field
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | 获取或设置数据字段的名称。 |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | 仅返回数据字段的名称。任何前缀都会被剥离到前缀属性中。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | 获取或设置该字段是否为映射字段。 |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | 获取或设置是否启用垂直格式的字符转换。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | 获取或设置在字段不为空时要在字段后插入的文本。 |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | 获取或设置在字段不为空时要在字段之前插入的文本。 |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | 获取 Microsoft Word 字段类型。 |

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

检索邮件合并主文档中合并字符内的数据字段的名称。 主文档与所选数据源合并时，将插入指定 数据字段中的信息来代替合并字段。

## 例子

演示如何使用 MERGEFIELD 字段来执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个数据表用作邮件合并数据源。
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// 插入一个 MERGEFIELD，其 FieldName 属性设置为数据源中列的名称。
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// 当合并发生时，我们可以在该字段接受的值之前和之后应用文本。
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// 为数据源中的不同列插入另一个 MERGEFIELD。
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
