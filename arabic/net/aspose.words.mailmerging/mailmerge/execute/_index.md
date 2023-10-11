---
title: MailMerge.Execute
second_title: Aspose.Words لمراجع .NET API
description: MailMerge طريقة. تنفيذ عملية دمج البريد من مصدر بيانات مخصص.
type: docs
weight: 180
url: /ar/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

تنفيذ عملية دمج البريد من مصدر بيانات مخصص.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | كائن يقوم بتطبيق واجهة مصدر بيانات دمج المراسلات المخصصة. |

### ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من أي مصدر بيانات مثل القائمة أو جدول التجزئة أو الكائنات. أنت بحاجة إلى كتابة فصلك الخاص الذي ينفذ[`IMailMergeDataSource`](../../imailmergedatasource/) واجهه المستخدم.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) يكون`خطأ شنيع`، أي أنك لا تحتاج إلى التوافق مع اللغة من اليمين إلى اليسار (مثل العربية أو العبرية).

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أنظر أيضا

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

تنفيذ عملية دمج البريد لسجل واحد.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldNames | String[] | مجموعة من أسماء حقول الدمج. أسماء الحقول ليست حساسة لحالة الأحرف. إذا تمت مصادفة اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| values | Object[] | صفيف القيم المراد إدراجه في حقول الدمج. يجب أن يكون عدد العناصر في هذا الصفيف هو نفس عدد العناصر الموجودة في*fieldNames*. |

### ملاحظات

استخدم هذا الأسلوب لملء حقول دمج البريد في المستند بقيم from صفيف من الكائنات.

تقوم هذه الطريقة بدمج البيانات لسجل واحد فقط. تمثل مجموعة الحقول name ومجموعة القيم بيانات سجل واحد.

لا يستخدم هذا الأسلوب مناطق دمج المراسلات.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أمثلة

يوضح كيفية دمج صورة من URI كبيانات دمج البريد في MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs ذات علامات "الصورة:" ستتلقى صورة أثناء عملية دمج البريد.
// السلسلة بعد النقطتين في علامة "الصورة:" تتوافق مع اسم العمود
// في مصدر البيانات الذي تحتوي خلاياه على معرفات URI لملفات الصور.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // قم بإنشاء مصدر بيانات يحتوي على معرفات URI للصور التي سنقوم بدمجها.
// يمكن أن يكون عنوان URI عنوان URL على الويب يشير إلى صورة، أو اسم ملف نظام ملفات محلي لملف صورة.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// تنفيذ دمج البريد على مصدر بيانات بصف واحد.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

يوضح كيفية إجراء دمج البريد، ثم حفظ المستند في مستعرض العميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// أرسل المستند إلى متصفح العميل.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); // تم طرحه لأن HttpResponse فارغ في الاختبار.

// سنحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من أننا لا نضيف أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

تنفيذ دمج البريد من DataTable في المستند.

```csharp
public void Execute(DataTable table)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| table | DataTable | الجدول الذي يحتوي على البيانات التي سيتم إدراجها في حقول دمج البريد. أسماء الحقول ليست حساسة لحالة الأحرف. إذا تمت مواجهة اسم حقل غير موجود في المستند، فسيتم تجاهله. |

### ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من a  **جدول البيانات**.

يتم دمج كافة السجلات من الجدول في المستند.

يمكنك استخدام الحقل التالي في مستند Word للتسبب[`MailMerge`](../) كائن لتحديد السجل التالي من **جدول البيانات** واستمر في الدمج. يمكن استخدام هذا عند إنشاء مستندات مثل الملصقات البريدية.

متى[`MailMerge`](../) يصل الكائن إلى نهاية المستند الرئيسي ولا يزال هناك المزيد من الصفوف في الملف **جدول البيانات**، يقوم بنسخ محتوى المستند الرئيسي بالكامل وإلحاقه بنهاية المستند الوجهة باستخدام فاصل section كفاصل.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام DataTable كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند واحد لدمج البريد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// إنشاء مستند مصدر لدمج البريد.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

يقوم بدمج البريد من **معرف البيانات** في المستند.

```csharp
public void Execute(IDataReader dataReader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataReader | IDataReader | مصدر البيانات لعملية دمج المراسلات. |

### ملاحظات

يمكنك تمرير **SqlDataReader** أو **OleDbDataReader** كائن في طريقة this كمعلمة لأن كلاهما تم تنفيذهما **معرف البيانات** واجهه المستخدم.

لاحظ أن هذا الأسلوب لا يستخدم مناطق دمج المراسلات وبالنسبة للسجلات المتعددة، فإن المستند سينمو عن طريق تكرار المستند بأكمله.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أمثلة

يوضح كيفية تشغيل دمج البريد باستخدام البيانات من قارئ البيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// قم بإنشاء سلسلة اتصال تشير إلى ملف قاعدة البيانات "Northwind".
// في نظام الملفات المحلي الخاص بنا، افتح اتصالاً وقم بإعداد استعلام SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // قم بإنشاء أمر SQL الذي سيصدر البيانات لدمج البريد لدينا.
    // أسماء أعمدة الجدول التي ستعيدها عبارة التحديد هذه
    // يجب أن يتوافق مع حقول الدمج التي وضعناها أعلاه.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {                    
        connection.Open();                 
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // خذ البيانات من القارئ واستخدمها في دمج البريد.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }                
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

يقوم بدمج البريد من a **عرض البيانات** في المستند.

```csharp
public void Execute(DataView dataView)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataView | DataView | مصدر البيانات لعملية دمج المراسلات. |

### ملاحظات

هذه الطريقة مفيدة إذا قمت باسترداد البيانات إلى ملف **جدول البيانات** ولكن ثم بحاجة إلى تطبيق عامل تصفية أو فرز قبل دمج البريد.

لاحظ أن هذا الأسلوب لا يستخدم مناطق دمج المراسلات وبالنسبة للسجلات المتعددة، فإن المستند سينمو عن طريق تكرار المستند بأكمله.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أمثلة

يوضح كيفية تحرير بيانات دمج البريد باستخدام DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// أنشئ جدول بيانات سيصدر منه دمج البريد البيانات.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// يمكننا استخدام طريقة عرض البيانات لتغيير بيانات دمج المراسلات دون إجراء تغييرات على جدول البيانات نفسه.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// يقوم عرض البيانات الخاص بنا بفرز الإدخالات بترتيب تنازلي على طول عمود "الدرجة".
// ويقوم بتصفية الصفوف ذات القيم الأقل من 50 في هذا العمود.
// ثلاثة من الصفوف الأربعة تناسب هذه المعايير بحيث يحتوي مستند الإخراج على ثلاث مستندات مدمجة.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

يقوم بدمج البريد من a **DataRow** في المستند.

```csharp
public void Execute(DataRow row)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| row | DataRow | الصف الذي يحتوي على بيانات سيتم إدراجها في حقول دمج البريد. أسماء الحقول ليست حساسة لحالة الأحرف. إذا تمت مواجهة اسم حقل غير موجود في المستند، فسيتم تجاهله. |

### ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من a **DataRow**.

تتجاهل هذه الطريقةRemoveUnusedRegions خيار.

### أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام DataTable كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند واحد لدمج البريد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// إنشاء مستند مصدر لدمج البريد.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


