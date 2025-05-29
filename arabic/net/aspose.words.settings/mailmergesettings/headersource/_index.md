---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية مصدر رأس MailMergeSettings، وحدد مسار رأس دمج البريد الخاص بك بسهولة. حسّن سير عمل مستنداتك اليوم!
type: docs
weight: 100
url: /ar/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

يحدد المسار إلى مصدر رأس الدمج البريدي. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string HeaderSource { get; set; }
```

## أمثلة

يوضح كيفية إنشاء مصدر بيانات لدمج البريد من مصدر الرأس ومصدر البيانات.

```csharp
// قم بإنشاء ملف رأس دمج ملصقات البريد، والذي سيتكون من جدول يحتوي على صف واحد.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// قم بإنشاء ملف بيانات دمج ملصقات البريد الذي يتكون من جدول يحتوي على صف واحد
 // ونفس عدد الأعمدة مثل جدول المستند الرئيسي.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// قم بإنشاء مستند وجهة دمج باستخدام MERGEFIELDS مع الأسماء التي
//تطابق أسماء الأعمدة في جدول ملف رأس الدمج.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// قم بإنشاء مصدر بيانات لدمج البريد الخاص بنا عن طريق تحديد اسمين لملفات المستندات.
// سيقوم مصدر الرأس بتسمية أعمدة جدول مصدر البيانات.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// سيوفر مصدر البيانات صفوفًا من البيانات لجميع الأعمدة الموجودة في جدول مستند الرأس.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// قم بتكوين دمج بريد من نوع ملصق بريدي، والذي سيقوم Microsoft Word بتنفيذه
//بمجرد أن نستخدمه لتحميل مستند الإخراج.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### أنظر أيضا

* class [MailMergeSettings](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
