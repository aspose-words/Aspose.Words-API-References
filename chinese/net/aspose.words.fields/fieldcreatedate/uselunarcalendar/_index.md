---
title: FieldCreateDate.UseLunarCalendar
second_title: Aspose.Words for .NET API 参考
description: FieldCreateDate 财产. 获取或设置是否使用回历农历或希伯来农历
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldcreatedate/uselunarcalendar/
---
## FieldCreateDate.UseLunarCalendar property

获取或设置是否使用回历农历或希伯来农历。

```csharp
public bool UseLunarCalendar { get; set; }
```

### 例子

演示如何使用 CREATEDATE 字段来显示文档的创建日期/时间。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// 我们可以使用 CREATEDATE 字段来显示文档的创建日期和时间。
// 下面是三种不同的日历类型，CREATEDATE 字段可以根据它们显示日期/时间。
// 1 - 伊斯兰农历：
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - 乌姆古拉历：
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
* 命名空间 [Aspose.Words.Fields](../../fieldcreatedate/)
* 部件 [Aspose.Words](../../../)


