---
title: Table.AllowAutoFit
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. يسمح لـ Microsoft Word و Aspose.Words بتغيير حجم الخلايا تلقائيًا في جدول لتلائم محتوياتها .
type: docs
weight: 50
url: /ar/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

يسمح لـ Microsoft Word و Aspose.Words بتغيير حجم الخلايا تلقائيًا في جدول لتلائم محتوياتها .

```csharp
public bool AllowAutoFit { get; set; }
```

### ملاحظات

النظام الأساسي`حقيقي`.

### أمثلة

يوضح كيفية تمكين / تعطيل تغيير حجم خلية الجدول التلقائي.

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

// اضبط خاصية "AllowAutoFit" على "false" للحصول على الجدول للحفاظ على الأبعاد
// من جميع صفوفه وخلاياه ، واقطع المحتويات إذا أصبحت كبيرة جدًا بحيث لا يمكن ملاءمتها.
// اضبط خاصية "AllowAutoFit" على "true" للسماح للجدول بتغيير عرض خلاياه وارتفاعها
// لاستيعاب محتوياتها.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


