---
title: RowFormat Class
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Tables.RowFormat لتنسيق شامل لصفوف الجداول. حسّن تصميم مستندك بميزات فعّالة ومرنة.
type: docs
weight: 7180
url: /ar/net/aspose.words.tables/rowformat/
---
## RowFormat class

يمثل كافة التنسيقات الخاصة بصف الجدول.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class RowFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | صحيح إذا كان من المسموح تقسيم النص الموجود في صف الجدول عبر فاصل الصفحة. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | يحصل على مجموعة حدود الخلايا الافتراضية للصف. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | صحيح إذا تم تكرار الصف كعنوان جدول في كل صفحة عندما يمتد الجدول إلى أكثر من صفحة واحدة. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | يحصل على ارتفاع صف الجدول بالنقاط أو يعينه. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | يحصل على القاعدة لتحديد ارتفاع صف الجدول أو يعينها. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | إعادة التعيين إلى تنسيق الصف الافتراضي. |

## أمثلة

يوضح كيفية تعديل تنسيق صف الجدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// استخدم خاصية "RowFormat" الخاصة بالصف الأول لتعيين التنسيق الذي يعدل مظهر الصف بأكمله.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

يوضح كيفية تعديل تنسيق الصفوف والخلايا في جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// استخدم خاصية "RowFormat" في الصف الأول لتعديل التنسيق
// من محتويات جميع الخلايا في هذا الصف.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

//استخدم خاصية "CellFormat" الخاصة بالخلية الأولى في الصف الأخير لتعديل تنسيق محتويات تلك الخلية.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
