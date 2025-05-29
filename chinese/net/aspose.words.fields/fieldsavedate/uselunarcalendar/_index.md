---
title: FieldSaveDate.UseLunarCalendar
linktitle: UseLunarCalendar
articleTitle: UseLunarCalendar
second_title: Aspose.Words for .NET
description: FieldSaveDate 的 UseLunarCalendar 属性允许您轻松地在伊斯兰历和希伯来历之间切换，以实现无缝的日期管理。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldsavedate/uselunarcalendar/
---
## FieldSaveDate.UseLunarCalendar property

获取或设置是否使用伊斯兰历或希伯来历。

```csharp
public bool UseLunarCalendar { get; set; }
```

## 例子

展示如何使用 SAVEDATE 字段显示使用 Microsoft Word 执行的文档最近一次保存操作的日期/时间。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// 我们可以使用 SAVEDATE 字段在文档上显示上次保存操作的日期和时间。
// 这些字段引用的保存操作是在 Microsoft Word 等应用程序中的手动保存，
// 不是文档的 Save 方法。
// 以下是三种不同的日历类型，SAVEDATE 字段可以根据这些日历类型显示日期/时间。
// 1 - 伊斯兰阴历：
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - 古兰经日历：
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - 印度国家日历：
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE 字段从 LastSavedTime 内置属性中提取其日期/时间值。
// 文档的Save方法不会更新这个值，但是我们仍然可以手动更新它。
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### 也可以看看

* class [FieldSaveDate](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
