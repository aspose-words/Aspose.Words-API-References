---
title: FieldDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words for .NET
description: 使用 FieldDate 的 UseLunarCalendar 属性优化您的日期管理。轻松在回历和希伯来阴历之间切换，增强功能。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fielddate/uselunarcalendar/
---
## FieldDate.UseLunarCalendar property

获取或设置是否使用伊斯兰历或希伯来历。

```csharp
public bool UseLunarCalendar { get; set; }
```

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

* class [FieldDate](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
