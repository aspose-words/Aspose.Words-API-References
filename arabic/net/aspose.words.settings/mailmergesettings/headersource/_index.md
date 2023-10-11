---
title: MailMergeSettings.HeaderSource
second_title: Aspose.Words لمراجع .NET API
description: MailMergeSettings ملكية. تحديد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة.
type: docs
weight: 100
url: /ar/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

تحديد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string HeaderSource { get; set; }
```

### أمثلة

يوضح كيفية إنشاء مصدر بيانات لدمج المراسلات من مصدر رأس ومصدر بيانات.

```csharp
// قم بإنشاء ملف رأس لدمج التسميات البريدية، والذي سيتكون من جدول به صف واحد.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// قم بإنشاء ملف بيانات لدمج الملصقات البريدية يتكون من جدول به صف واحد
 // ونفس عدد الأعمدة الموجودة في جدول مستند الرأس.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// قم بإنشاء مستند وجهة دمج باستخدام MERGEFIELDS بأسماء ذلك
// تطابق أسماء الأعمدة في جدول ملف رأس الدمج.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// أنشئ مصدر بيانات لدمج البريد الخاص بنا عن طريق تحديد اسمين لملفات المستندات.
// سيقوم مصدر الرأس بتسمية أعمدة جدول مصدر البيانات.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// سيوفر مصدر البيانات صفوفًا من البيانات لجميع الأعمدة في جدول مستند الرأس.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// قم بتكوين دمج البريد من نوع التسمية البريدية، والذي سيقوم Microsoft Word بتنفيذه
// بمجرد استخدامه لتحميل مستند الإخراج.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### أنظر أيضا

* class [MailMergeSettings](../)
* مساحة الاسم [Aspose.Words.Settings](../../mailmergesettings/)
* المجسم [Aspose.Words](../../../)


