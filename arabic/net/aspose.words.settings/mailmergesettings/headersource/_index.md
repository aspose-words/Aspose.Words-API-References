---
title: MailMergeSettings.HeaderSource
second_title: Aspose.Words لمراجع .NET API
description: MailMergeSettings ملكية. يحدد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة.
type: docs
weight: 100
url: /ar/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

يحدد المسار إلى مصدر رأس دمج المراسلات. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string HeaderSource { get; set; }
```

### أمثلة

يوضح كيفية إنشاء مصدر بيانات لدمج البريد من مصدر رأس ومصدر بيانات.

```csharp
// إنشاء ملف رأس دمج تسمية بريدية ، والذي سيتكون من جدول به صف واحد.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// إنشاء ملف بيانات دمج تسمية بريدية يتكون من جدول به صف واحد
// ونفس عدد أعمدة جدول مستند الرأس. 
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// إنشاء مستند وجهة دمج مع MERGEFIELDS بأسماء تلك
// تطابق أسماء الأعمدة في جدول ملف رأس الدمج.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// إنشاء مصدر بيانات لدمج البريد الخاص بنا عن طريق تحديد اسمي ملف مستند.
// سيقوم مصدر الرأس بتسمية أعمدة جدول مصدر البيانات.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// سيوفر مصدر البيانات صفوفًا من البيانات لجميع الأعمدة في جدول مستند الرأس.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// تكوين دمج بريد بنوع تسمية بريدية ، والذي سينفذه Microsoft Word
// بمجرد استخدامه لتحميل المستند الناتج.
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


