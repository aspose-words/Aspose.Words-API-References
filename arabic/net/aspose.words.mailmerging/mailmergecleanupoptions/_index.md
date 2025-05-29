---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.MailMergeCleanupOptions لإدارة عملية تنظيف دمج البريد بكفاءة. حسّن مستنداتك بالتحكم في إزالة العناصر بسلاسة.
type: docs
weight: 4540
url: /ar/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

يحدد الخيارات التي تحدد العناصر التي سيتم إزالتها أثناء دمج البريد.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد قيمة افتراضية. |
| RemoveEmptyParagraphs | `1` | يحدد ما إذا كان يجب إزالة الفقرات التي تحتوي على حقول دمج البريد بدون بيانات من المستند. عندما يتم تعيين هذا الخيار، تتم أيضًا إزالة الفقرات التي تحتوي على حقول دمج بداية ونهاية المنطقة والتي تكون فارغة بخلاف ذلك . |
| RemoveUnusedRegions | `2` | يحدد ما إذا كان يجب إزالة مناطق دمج البريد غير المستخدمة من المستند. |
| RemoveUnusedFields | `4` | يحدد ما إذا كان يجب إزالة حقول الدمج غير المستخدمة من المستند. |
| RemoveContainingFields | `8` | يحدد ما إذا كان يجب إزالة الحقول التي تحتوي على حقول دمج (على سبيل المثال، IFs) من document إذا تمت إزالة حقول الدمج المتداخلة. |
| RemoveStaticFields | `10` | يُحدد ما إذا كان يجب إزالة الحقول الثابتة من المستند. الحقول الثابتة هي الحقول التي تبقى نتائجها كما هي عند أي تغيير في المستند. الحقول التي لا تُخزّن نتائجها في document وتُحسب تلقائيًا (مثلFieldListNum ، FieldSymbol ، إلخ) لا تعتبر ثابتة. |
| RemoveEmptyTableRows | `20` | يحدد ما إذا كان يجب إزالة الصفوف الفارغة التي تحتوي على مناطق دمج البريد من المستند. |
| RemoveEmptyTables | `40` | يحدد ما إذا كان سيتم الإزالة من جداول المستندات التي تحتوي على مناطق دمج البريد التي تمت إزالتها باستخدام إماRemoveUnusedRegions أو الRemoveEmptyTableRows الخيار. |

## أمثلة

يوضح كيفية إزالة الجدول الفارغ بالكامل أثناء دمج البريد.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

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

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
