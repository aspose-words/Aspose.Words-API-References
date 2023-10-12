---
title: FieldDate.UseUmAlQuraCalendar
second_title: Aspose.Words for .NET API 参考
description: FieldDate 财产. 获取或设置是否使用 UmalQura 日历
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fielddate/useumalquracalendar/
---
## FieldDate.UseUmAlQuraCalendar property

获取或设置是否使用 Um-al-Qura 日历。

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

### 例子

演示如何使用 DATE 字段根据不同类型的日历显示日期。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们希望文档中的文本始终显示正确的日期，我们可以使用 DATE 字段。
// 下面是 DATE 字段可用来显示日期的三种文化日历。
// 1 - 伊斯兰农历：
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - 乌姆古拉历：
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - 印度国家日历：
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// 插入一个日期字段并将其日历类型设置为主机应用程序最后使用的日历类型。
// 在 Microsoft Word 中，该类型将是插入 -> 中最近使用的类型文字->日期和时间对话框。
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### 也可以看看

* class [FieldDate](../)
* 命名空间 [Aspose.Words.Fields](../../fielddate/)
* 部件 [Aspose.Words](../../../)


