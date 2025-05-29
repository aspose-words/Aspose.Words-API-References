---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Tables.CellFormat لتنسيق شامل لخلايا الجدول. حسّن تنسيق مستنداتك بميزات سهلة الاستخدام!
type: docs
weight: 7110
url: /ar/net/aspose.words.tables/cellformat/
---
## CellFormat class

يمثل كافة التنسيقات لخلية الجدول.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class CellFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | يحصل على مجموعة من حدود الخلية. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | يقوم بإرجاع أو تعيين مقدار المساحة (بالنقاط) التي يجب إضافتها أسفل محتويات الخلية. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | إذا`حقيقي` ، يلائم النص في الخلية، ويضغط كل فقرة على عرض الخلية. |
| [HideMark](../../aspose.words.tables/cellformat/hidemark/) { get; set; } | يعيد أو يحدد إمكانية رؤية علامة الخلية. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | يحدد كيفية دمج الخلية أفقيًا مع الخلايا الأخرى في الصف. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | يقوم بإرجاع أو تعيين مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يسار محتويات الخلية. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | إرجاع أو تعيين اتجاه النص في خلية الجدول. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | يعيد أو يعين العرض المفضل للخلية. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | يقوم بإرجاع أو تعيين مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يمين محتويات الخلية. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | يعيد[`Shading`](../../aspose.words/shading/) الكائن الذي يشير إلى تنسيق التظليل للخلية. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | يقوم بإرجاع أو تعيين مقدار المساحة (بالنقاط) المراد إضافتها فوق محتويات الخلية. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | يعيد أو يضبط المحاذاة الرأسية للنص في الخلية. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | يحدد كيفية دمج الخلية مع الخلايا الأخرى عموديًا. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | يحصل على عرض الخلية بالنقاط. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | إذا`حقيقي` , التفاف النص للخلية. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | يُعيد ضبط تنسيق الخلية الافتراضي. لا يُغيّر عرض الخلية. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | يحدد مقدار المساحة (بالنقاط) التي يجب إضافتها إلى اليسار/الأعلى/اليمين/الأسفل من محتويات الخلية. |

## أمثلة

يوضح كيفية تعديل تنسيق خلية الجدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// استخدم خاصية "CellFormat" الخاصة بالخلية لتعيين التنسيق الذي يعدل مظهر تلك الخلية.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
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
