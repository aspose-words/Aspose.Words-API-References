---
title: CellFormat.WrapText
linktitle: WrapText
articleTitle: WrapText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CellFormat WrapText لتحسين قابلية قراءة جدول البيانات الخاص بك عن طريق لف النص تلقائيًا في الخلايا للحصول على مظهر أنظف.
type: docs
weight: 150
url: /ar/net/aspose.words.tables/cellformat/wraptext/
---
## CellFormat.WrapText property

إذا`حقيقي` , التفاف النص للخلية.

```csharp
public bool WrapText { get; set; }
```

## أمثلة

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

* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
