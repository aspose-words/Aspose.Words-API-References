---
title: FieldDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: 用于 .NET 的 Aspose.Words
description: FieldDate UseSakaEraCalendar 财产. 获取或设置是否使用Saka Era日历 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fielddate/usesakaeracalendar/
---
## FieldDate.UseSakaEraCalendar property

获取或设置是否使用Saka Era日历。

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## 例子

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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
