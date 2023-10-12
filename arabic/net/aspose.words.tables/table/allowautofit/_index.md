---
title: Table.AllowAutoFit
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. يسمح لـ Microsoft Word وAspose.Words بتغيير حجم الخلايا تلقائيًا في الجدول لتناسب محتوياتها.
type: docs
weight: 50
url: /ar/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

يسمح لـ Microsoft Word وAspose.Words بتغيير حجم الخلايا تلقائيًا في الجدول لتناسب محتوياتها.

```csharp
public bool AllowAutoFit { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي`.

### أمثلة

يوضح كيفية تمكين/تعطيل تغيير الحجم التلقائي لخلية الجدول.

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

// اضبط خاصية "AllowAutoFit" على "خطأ" للحصول على جدول يحافظ على الأبعاد
// لجميع صفوفه وخلاياه، واقتطاع المحتويات إذا أصبحت كبيرة جدًا بحيث لا يمكن احتواؤها.
// اضبط الخاصية "AllowAutoFit" على "صحيح" للسماح للجدول بتغيير عرض الخلايا وارتفاعها
// لاستيعاب محتوياتها.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


