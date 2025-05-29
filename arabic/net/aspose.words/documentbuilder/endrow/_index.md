---
title: DocumentBuilder.EndRow
linktitle: EndRow
articleTitle: EndRow
second_title: Aspose.Words لـ .NET
description: أنهِ صفوف الجداول في مستنداتك بسهولة باستخدام طريقة EndRow من DocumentBuilder. بسّط تنسيقك وحسّن وضوح مستندك!
type: docs
weight: 240
url: /ar/net/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder.EndRow method

ينهي صف جدول في المستند.

```csharp
public Row EndRow()
```

### قيمة الإرجاع

عقدة الصف التي تم الانتهاء منها للتو.

## ملاحظات

يتصل`EndRow` لإنهاء صف الجدول. إذا اتصلت[`InsertCell`](../insertcell/) بعد ذلك مباشرة ، يستمر الجدول في صف جديد.

استخدم[`RowFormat`](../rowformat/) الخاصية لتحديد تنسيق الصف.

## أمثلة

يوضح كيفية دمج خلايا الجدول عموديا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية هي الأولى في نطاق الخلايا المندمجة عموديًا.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

//أدرج خلية في العمود الثاني من الصف الأول، ثم أنهِ الصف.
// قم أيضًا بتكوين المنشئ لتعطيل الدمج الرأسي في الخلايا التي تم إنشاؤها.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 //أدرج خلية في العمود الأول من الصف الثاني.
//بدلاً من إضافة محتويات النص، سنقوم بدمج هذه الخلية مع الخلية الأولى التي أضفناها مباشرة أعلاه.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// أدخل خلية مستقلة أخرى في العمود الثاني من الصف الثاني.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

يوضح كيفية إنشاء جدول 2x2 منسق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// أثناء إنشاء الجدول، سيقوم منشئ المستند بتطبيق قيم خصائص RowFormat/CellFormat الحالية
// إلى الصف/الخلية الحالية التي يتواجد بها المؤشر وأي صفوف/خلايا جديدة أثناء إنشائها.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// لا تتأثر الصفوف والخلايا المضافة مسبقًا بأثر رجعي بالتغييرات التي تطرأ على تنسيق المنشئ.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

يوضح كيفية إنشاء جدول بحدود مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

//إعداد خيارات تنسيق الجدول لمنشئ المستندات
// سيتم تطبيقها على كل صف وخلية نضيفها معها.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// سيؤدي تغيير التنسيق إلى تطبيقه على الخلية الحالية،
//وأي خلايا جديدة نقوم بإنشائها باستخدام المنشئ بعد ذلك.
// لن يؤثر هذا على الخلايا التي أضفناها مسبقًا.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// زيادة ارتفاع الصف ليتناسب مع النص الرأسي.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### أنظر أيضا

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
