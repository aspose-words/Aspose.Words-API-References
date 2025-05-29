---
title: FieldCreateDate.UseUmAlQuraCalendar
linktitle: UseUmAlQuraCalendar
articleTitle: UseUmAlQuraCalendar
second_title: Aspose.Words for .NET
description: 使用 FieldCreateDate 的 UseUmAlQuraCalendar 属性轻松管理日期格式。切换到 UmalQura 日历可实现精确的日期处理。
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

获取或设置是否使用 Um-al-Qura 日历。

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

## 例子

展示如何使用 CREATEDATE 字段显示文档的创建日期/时间。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// 我们可以使用 CREATEDATE 字段来显示文档的创建日期和时间。
// 以下是三种不同的日历类型，CREATEDATE 字段可以根据这些日历类型显示日期/时间。
// 1 - 伊斯兰阴历：
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - 古兰经日历：
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

* class [FieldCreateDate](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
