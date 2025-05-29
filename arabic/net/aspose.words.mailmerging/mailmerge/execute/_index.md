---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words لـ .NET
description: قم بتبسيط عملية البريد الخاصة بك باستخدام طريقة MailMerge Execute، والتي تعمل على دمج البيانات بسهولة من مصادر مخصصة لتوفير اتصالات مخصصة.
type: docs
weight: 180
url: /ar/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | كائن ينفذ واجهة مصدر بيانات دمج البريد المخصصة. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من أي مصدر بيانات، مثل قائمة أو جدول تجزئة أو كائنات. ستحتاج إلى كتابة فئة خاصة بك تُطبّق [`IMailMergeDataSource`](../../imailmergedatasource/) واجهة.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) يكون`خطأ شنيع`, وهذا يعني أنك لا تحتاج إلى توافق اللغة من اليمين إلى اليسار (مثل العربية أو العبرية).

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

يوضح كيفية تنفيذ دمج البريد مع مصدر البيانات في شكل كائن مخصص.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // لاستخدام كائن مخصص كمصدر بيانات، يجب عليه تنفيذ واجهة IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// مثال على فئة "كيان البيانات" في تطبيقك.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// مصدر بيانات دمج البريد المخصص الذي تقوم بتنفيذه للسماح لـ Aspose.Words
/// لدمج البيانات من كائنات العميل الخاصة بك في مستندات Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // عندما نقوم بتهيئة مصدر البيانات، يجب أن يكون موضعه قبل السجل الأول.
        mRecordIndex = -1;
    }

    /// <summary>
    /// اسم مصدر البيانات. يُستخدم بواسطة Aspose.Words فقط عند تنفيذ دمج البريد مع مناطق قابلة للتكرار.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// تستدعي Aspose.Words هذه الطريقة للحصول على قيمة لكل حقل بيانات.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // قم بإرجاع "false" إلى محرك دمج البريد Aspose.Words للإشارة إلى
                // لم نتمكن من العثور على حقل بهذا الاسم.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// تنفيذ قياسي للانتقال إلى السجل التالي في المجموعة.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### أنظر أيضا

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

ينفذ عملية دمج البريد لسجل واحد.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldNames | String[] | مجموعة من أسماء حقول الدمج. أسماء الحقول لا تفرق بين الأحرف الكبيرة والصغيرة. إذا وُجد اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| values | Object[] | مجموعة من القيم التي سيتم إدراجها في حقول الدمج. يجب أن يكون عدد العناصر في هذه المجموعة مساويًا لعدد العناصر في*fieldNames*. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من مجموعة من الكائنات.

تدمج هذه الطريقة بيانات سجل واحد فقط. تُمثل مصفوفة أسماء الحقول ومصفوفة القيم بيانات سجل واحد.

لا تستخدم هذه الطريقة مناطق دمج البريد.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

يوضح كيفية دمج صورة من عنوان URI كبيانات دمج بريد في MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// ستتلقى حقول الدمج التي تحتوي على علامات "Image:" صورة أثناء دمج البريد.
// السلسلة بعد النقطتين في علامة "Image:" تتوافق مع اسم العمود
// في مصدر البيانات الذي تحتوي خلاياه على عناوين URI لملفات الصور.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // قم بإنشاء مصدر بيانات يحتوي على عناوين URI للصور التي سنقوم بدمجها.
// يمكن أن يكون URI عنوان URL للويب يشير إلى صورة، أو اسم ملف نظام ملفات محلي لملف صورة.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

//تنفيذ دمج البريد على مصدر بيانات يحتوي على صف واحد.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

يوضح كيفية تنفيذ عملية دمج البريد، ثم حفظ المستند في متصفح العميل.

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

//إرسال المستند إلى متصفح العميل.
//تم إلقاؤه لأن HttpResponse فارغ في الاختبار.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// سوف نحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من عدم إضافة أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.Throws<NullReferenceException>(() => response.End());
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

يقوم بدمج البريد من جدول بيانات إلى المستند.

```csharp
public void Execute(DataTable table)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| table | DataTable | جدول يحتوي على بيانات سيتم إدراجها في حقول دمج البريد. أسماء الحقول ليست حساسة لحالة الأحرف. إذا تم العثور على اسم حقل غير موجود في المستند، فسيتم تجاهله. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بالقيم من a **جدول البيانات**.

سيتم دمج كافة السجلات من الجدول في المستند.

يمكنك استخدام الحقل التالي في مستند Word للتسبب في[`MailMerge`](../) كائن لتحديد السجل التالي من**جدول البيانات** ويمكن استخدام هذا عند إنشاء مستندات مثل ملصقات البريد.

متى[`MailMerge`](../) يصل الكائن إلى نهاية المستند الرئيسي ولا يزال هناك المزيد من الصفوف في**جدول البيانات**، فإنه ينسخ المحتوى الكامل لـ المستند الرئيسي ويضيفه إلى نهاية المستند الوجهة باستخدام فاصل section كفاصل.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من جدول البيانات.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام جدول البيانات كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريدي واحد:
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
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

يقوم بدمج البريد من**قارئ بيانات الهوية** في المستند.

```csharp
public void Execute(IDataReader dataReader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataReader | IDataReader | مصدر البيانات لعملية دمج البريد. |

## ملاحظات

يمكنك المرور**قارئ بيانات SQL** أو**قارئ بيانات OleDb**الكائن في طريقة this كمعلمة لأن كلاهما تم تنفيذه**قارئ بيانات الهوية** واجهة.

لاحظ أن هذه الطريقة لا تستخدم مناطق دمج البريد وبالنسبة للسجلات المتعددة فإن مستند the سوف ينمو عن طريق تكرار المستند بأكمله.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

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

// إنشاء سلسلة اتصال تشير إلى ملف قاعدة البيانات "Northwind"
// في نظام الملفات المحلي لدينا، افتح اتصالاً، وقم بإعداد استعلام SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // قم بإنشاء أمر SQL الذي سيقوم بتوريد البيانات لعملية دمج البريد الخاصة بنا.
    // أسماء أعمدة الجدول التي ستعيدها عبارة SELECT هذه
    // سوف تحتاج إلى التوافق مع حقول الدمج التي وضعناها أعلاه.
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
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

يقوم بدمج البريد من**عرض البيانات** في المستند.

```csharp
public void Execute(DataView dataView)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataView | DataView | مصدر البيانات لعملية دمج البريد. |

## ملاحظات

هذه الطريقة مفيدة إذا كنت ترغب في استرداد البيانات في**جدول البيانات** ولكن بعد ذلك، يجب تطبيق عامل تصفية أو فرز قبل دمج البريد.

لاحظ أن هذه الطريقة لا تستخدم مناطق دمج البريد وبالنسبة للسجلات المتعددة فإن مستند the سوف ينمو عن طريق تكرار المستند بأكمله.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

يوضح كيفية تحرير بيانات دمج البريد باستخدام DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// قم بإنشاء جدول بيانات سيستمد منه دمج البريد الخاص بنا البيانات.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// يمكننا استخدام عرض البيانات لتعديل بيانات دمج البريد دون إجراء أي تغييرات على جدول البيانات نفسه.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// يقوم عرض البيانات لدينا بفرز الإدخالات بترتيب تنازلي على طول عمود "الدرجة"
// ويقوم بتصفية الصفوف التي تحتوي على قيم أقل من 50 في هذا العمود.
// ثلاثة من الصفوف الأربعة تتناسب مع هذه المعايير بحيث تحتوي وثيقة الإخراج على ثلاثة مستندات دمج.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

يقوم بدمج البريد من**صف البيانات** في المستند.

```csharp
public void Execute(DataRow row)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| row | DataRow | صف يحتوي على بيانات سيتم إدراجها في حقول دمج البريد. أسماء الحقول ليست حساسة لحالة الأحرف. إذا تم العثور على اسم حقل غير موجود في المستند، فسيتم تجاهله. |

## ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من**صف البيانات**.

هذه الطريقة تتجاهلRemoveUnusedRegions خيار.

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من جدول البيانات.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام جدول البيانات كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريدي واحد:
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
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
