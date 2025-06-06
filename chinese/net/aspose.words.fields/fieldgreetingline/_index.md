---
title: FieldGreetingLine Class
linktitle: FieldGreetingLine
articleTitle: FieldGreetingLine
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldGreetingLine 类，旨在轻松实现 GREETINGLINE 字段以增强文档个性化。
type: docs
weight: 2390
url: /zh/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

实现 GREETINGLINE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldGreetingLine : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | 如果名称为空，则获取或设置要包含在字段中的文本。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | 获取或设置用于格式化名称的语言 ID。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | 获取或设置字段中包含的名称的格式。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | 返回该字段使用的邮件合并字段名称的集合。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

插入邮件合并问候语。

## 例子

显示如何插入 GREETINGLINE 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 GREETINGLINE 字段创建通用问候语，并在其后添加一些文本。
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// GREETINGLINE 字段在邮件合并期间接受来自数据源的值，就像 MERGEFIELD 一样。
// 它还可以格式化邮件合并完成后源数据在其位置的写入方式。
// 字段名称集合对应于数据源中的列
// 该字段将从中获取值。
Assert.AreEqual(0, field.GetFieldNames().Length);

// 为了填充该数组，我们需要为问候语指定一种格式。
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// 现在，我们的字段将接受数据源中这两列的值。
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// 此字符串将涵盖任何数据表数据无效的情况
// 通过用字符串替换格式错误的名称。
field.AlternateText = "Sir or Madam";

// 设置语言环境来格式化结果。
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// 创建一个数据表，其列名与元素匹配
// 从字段的字段名称集合中，然后执行邮件合并。
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// 此行在礼节称谓列中具有无效值，因此我们的问候语将默认为替代文本。
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
