---
title: MailMerge.CleanupOptions
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

الحصول على أو تعيين مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

### أمثلة

يوضح كيفية إزالة الفقرات الفارغة التي قد تنشئها عملية دمج البريد من مستند إخراج الدمج.

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

يوضح كيفية إزالة MERGEFIELD التي لا يتم استخدامها أثناء دمج البريد تلقائيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء مستند باستخدام MERGEFIELDs لثلاثة أعمدة من جدول مصدر بيانات دمج المراسلات،
// ثم قم بإنشاء جدول يحتوي على عمودين فقط تتطابق أسماؤهما مع MERGEFIELDs الخاصة بنا.
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

// يشير MERGEFIELD الثالث إلى عمود "المدينة"، وهو غير موجود في مصدر البيانات لدينا.
// سوف يترك دمج البريد الحقول مثل هذه سليمة في حالتها السابقة للدمج.
// سيؤدي تعيين خاصية "CleanupOptions" على "RemoveUnusedFields" إلى إزالة أي MERGEFIELDs
// التي لا يتم استخدامها أثناء عملية دمج البريد لتنظيف مستندات الدمج.
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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


