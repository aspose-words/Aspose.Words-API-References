---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words لـ .NET
description: OutlineOptions CreateOutlinesForHeadingsInTables ملكية. يحدد ما إذا كان سيتم إنشاء مخططات تفصيلية للعناوين الفقرات المنسقة باستخدام أنماط العناوين داخل الجداول أم لا في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

يحدد ما إذا كان سيتم إنشاء مخططات تفصيلية للعناوين (الفقرات المنسقة باستخدام أنماط العناوين) داخل الجداول أم لا.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية إنشاء إدخالات مخطط تفصيلي لمستند PDF للعناوين داخل الجداول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء جدول بثلاثة صفوف. الصف الأول،
// الذي سنقوم بتنسيق نصه بنمط نوع العنوان، سيكون بمثابة رأس العمود.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// اضبط خاصية "HeadingsOutlineLevels" على "1" للحصول على المخطط التفصيلي
// لتسجيل العناوين التي لا يزيد حجمها عن 1 فقط.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// قم بتعيين الخاصية "CreateOutlinesForHeadingsInTables" على "خطأ" لاستبعاد كافة العناوين الموجودة داخل الجداول،
// مثل الذي أنشأناه أعلاه من المخطط التفصيلي.
// قم بتعيين الخاصية "CreateOutlinesForHeadingsInTables" على "صحيح" لتضمين كافة العناوين داخل الجداول
// في المخطط التفصيلي، بشرط أن يكون لديهم مستوى عنوان لا يزيد عن قيمة خاصية "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
