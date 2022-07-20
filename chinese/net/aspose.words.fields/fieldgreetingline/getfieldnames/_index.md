---
title: GetFieldNames
second_title: Aspose.Words for .NET API 参考
description: 返回字段使用的邮件合并字段名称的集合
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldgreetingline/getfieldnames/
---
## FieldGreetingLine.GetFieldNames method

返回字段使用的邮件合并字段名称的集合。

```csharp
public string[] GetFieldNames()
```

### 例子

显示如何插入 GREETINGLINE 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 GREETINGLINE 字段创建通用问候语，并在其后添加一些文本。
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// GREETINGLINE 字段在邮件合并期间接受来自数据源的值，例如 MERGEFIELD。
// 一旦邮件合并完成，它还可以格式化源数据在其位置上的写入方式。
// 字段名称集合对应于数据源中的列
// 该字段将从中获取值。
Assert.AreEqual(0, field.GetFieldNames().Length);

// 要填充该数组，我们需要为我们的问候语指定格式。
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// 现在，我们的字段将接受数据源中这两列的值。
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// 该字符串将涵盖任何数据表数据无效的情况
// 通过用字符串替换格式错误的名称。
field.AlternateText = "Sir or Madam";

// 设置区域设置以格式化结果。
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// 创建一个数据表，其中包含名称与元素匹配的列
// 从字段的字段名集合中，然后进行邮件合并。
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// 此行在 Courtesy Title 列中的值无效，因此我们的问候语将默认为备用文本。
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### 也可以看看

* class [FieldGreetingLine](../../fieldgreetingline)
* 命名空间 [Aspose.Words.Fields](../../fieldgreetingline)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->