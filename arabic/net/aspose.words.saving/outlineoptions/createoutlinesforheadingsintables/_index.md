---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية CreateOutlinesForHeadingsInTables على تعزيز تنظيم الجدول من خلال تمكين الخطوط العريضة لأنماط العناوين، مما يحسن وضوح المستند.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة باستخدام أنماط العناوين) داخل الجداول أم لا.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية إنشاء إدخالات مخطط مستند PDF للعناوين داخل الجداول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ جدولًا بثلاثة صفوف. الصف الأول،
// الذي سنقوم بتنسيق النص الخاص به بنمط نوع العنوان، سيكون بمثابة رأس العمود.
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

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// اضبط خاصية "HeadingsOutlineLevels" على "1" للحصول على المخطط التفصيلي
// لتسجيل العناوين فقط بمستويات عناوين لا يزيد حجمها عن 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// اضبط خاصية "CreateOutlinesForHeadingsInTables" على "false" لاستبعاد جميع العناوين داخل الجداول،
// مثل الذي أنشأناه أعلاه من المخطط التفصيلي.
// اضبط خاصية "CreateOutlinesForHeadingsInTables" على "true" لتضمين جميع العناوين داخل الجداول
// في المخطط التفصيلي، بشرط أن يكون مستوى العنوان ليس أكبر من قيمة الخاصية "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
