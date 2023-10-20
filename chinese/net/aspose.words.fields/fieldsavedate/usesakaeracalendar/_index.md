---
title: FieldSaveDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: 用于 .NET 的 Aspose.Words
description: FieldSaveDate UseSakaEraCalendar 财产. 获取或设置是否使用Saka Era日历 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

获取或设置是否使用Saka Era日历。

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## 例子

演示如何使用 SAVEDATE 字段来显示最近使用 Microsoft Word 执行的文档保存操作的日期/时间。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// 我们可以使用 SAVEDATE 字段来显示文档上最后一次保存操作的日期和时间。
// 这些字段所指的保存操作是在Microsoft Word等应用程序中的手动保存，
// 不是文档的 Save 方法。
// 下面是三种不同的日历类型，根据这些类型，SAVEDATE 字段可以显示日期/时间。
// 1 - 伊斯兰农历：
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - 乌姆古拉历：
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - 印度国家日历：
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE 字段从 LastSavedTime 内置属性中提取日期/时间值。
// 文档的Save方法不会更新这个值，但我们仍然可以手动更新它。
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### 也可以看看

* class [FieldSaveDate](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
