---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table AllowAutoFit لتغيير حجم خلايا جدول Microsoft Word و Aspose.Words بسهولة، مما يعزز قابلية قراءة مستندك وعرضه.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

يسمح لبرنامج Microsoft Word وAspose.Words بتغيير حجم الخلايا في الجدول تلقائيًا لتناسب محتوياتها.

```csharp
public bool AllowAutoFit { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية تمكين/تعطيل تغيير حجم خلايا الجدول تلقائيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// اضبط خاصية "AllowAutoFit" على "false" لجعل الجدول يحافظ على الأبعاد
// لجميع صفوفها وخلاياها، وقم بتقليص المحتويات إذا أصبحت كبيرة جدًا بحيث لا تتناسب مع المساحة.
// اضبط خاصية "AllowAutoFit" على "true" للسماح للجدول بتغيير عرض وارتفاع خلاياه
// لاستيعاب محتوياتها.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
