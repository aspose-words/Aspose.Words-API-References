---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertCell في DocumentBuilder—أضف بسرعة خلايا جدول قابلة للتخصيص لتحسين التنظيم والوضوح.
type: docs
weight: 270
url: /ar/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

إدراج خلية جدول في المستند.

```csharp
public Cell InsertCell()
```

### قيمة الإرجاع

عقدة الخلية التي تم إدخالها للتو.

## ملاحظات

لبدء جدول، فقط اتصل`InsertCell` . بعد ذلك، سيتم إضافة أي محتوى تقوم بإضافته باستخدام طرق أخرى من[`DocumentBuilder`](../) سيتم إضافة الفصل إلى الخلية الحالية.

لبدء خلية جديدة في نفس الصف، اتصل بـ`InsertCell` مرة أخرى.

لإنهاء استدعاء صف الجدول[`EndRow`](../endrow/).

استخدم[`CellFormat`](../cellformat/) الخاصية لتحديد تنسيق الخلية.

## أمثلة

يوضح كيفية استخدام منشئ المستندات لإنشاء جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ابدأ الجدول، ثم املأ الصف الأول بخليتين.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

//استدعاء طريقة "EndRow" الخاصة بالمنشئ لبدء صف جديد.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
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

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
