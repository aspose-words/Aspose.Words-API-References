---
title: FieldPrintDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: 用于 .NET 的 Aspose.Words
description: FieldPrintDate UseSakaEraCalendar 财产. 获取或设置是否使用Saka Era日历 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldprintdate/usesakaeracalendar/
---
## FieldPrintDate.UseSakaEraCalendar property

获取或设置是否使用Saka Era日历。

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## 例子

显示读取的 PRINTDATE 字段。

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// 当文档被打印机打印或打印为 PDF（但未导出为 PDF）时，
// PRINTDATE 字段将显示打印操作的日期/时间。
// 如果没有进行打印，这些字段将显示“0/0/0000”。
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// 下面是三种不同的日历类型，根据它们的 PRINTDATE 字段
// 可以显示上次打印操作的日期和时间。
// 1 - 伊斯兰农历：
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - 乌姆古拉历：
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

* class [FieldPrintDate](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
