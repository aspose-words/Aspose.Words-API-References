---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words لـ .NET
description: قم بتحسين عملية دمج البريد لديك باستخدام خاصية CleanupOptions—يمكنك بسهولة إدارة العناصر التي تريد إزالتها للحصول على عملية سلسة وفعالة.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

يحصل على مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد أو يعينها.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## أمثلة

يوضح كيفية إزالة الفقرات الفارغة التي قد ينشئها دمج البريد من مستند إخراج الدمج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

يوضح كيفية إزالة MERGEFIELDs تلقائيًا والتي لا يتم استخدامها أثناء دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء مستند يحتوي على MERGEFIELDs لثلاثة أعمدة من جدول مصدر بيانات دمج البريد،
// ثم قم بإنشاء جدول يحتوي على عمودين فقط يتطابق اسميهما مع MERGEFIELDs الخاصة بنا.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// يشير حقل MERGEFIELD الثالث لدينا إلى عمود "المدينة"، والذي لا يوجد في مصدر البيانات الخاص بنا.
// سيؤدي دمج البريد إلى ترك الحقول مثل هذا سليمة في حالتها قبل الدمج.
// سيؤدي تعيين خاصية "CleanupOptions" إلى "RemoveUnusedFields" إلى إزالة أي MERGEFIELDs
// التي لا يتم استخدامها أثناء دمج البريد لتنظيف مستندات الدمج.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### أنظر أيضا

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
