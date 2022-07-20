---
title: Execute
second_title: Aspose.Words لمراجع .NET API
description: يقوم بإجراء دمج بريد من مصدر بيانات مخصص.
type: docs
weight: 180
url: /ar/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

يقوم بإجراء دمج بريد من مصدر بيانات مخصص.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | كائن يقوم بتنفيذ واجهة مصدر بيانات دمج المراسلات المخصصة. |

### ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من_ x000d_ أي مصدر بيانات مثل قائمة أو قابل للتجزئة أو كائنات. تحتاج إلى كتابة your class الخاص الذي يقوم بتنفيذ ملف[`IMailMergeDataSource`](../../imailmergedatasource) واجهه المستخدم.

يمكنك استخدام هذه الطريقة فقط عندما[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)خطأ ، يعني أنك لا تحتاج إلى توافق مع لغة من اليمين إلى اليسار (مثل العربية أو العبرية).

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

### أنظر أيضا

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

تنفيذ عملية دمج المراسلات لسجل واحد.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldNames | String[] | صفيف من أسماء حقول الدمج. أسماء الحقول ليست حساسة لحالة الأحرف . إذا تمت مصادفة اسم حقل غير موجود في المستند ، فسيتم تجاهله. |
| values | Object[] | صفيف من القيم المراد إدراجها في حقول الدمج. يجب أن يكون عدد العناصر في هذه المصفوفة هو نفسه عدد العناصر في fieldNames. |

### ملاحظات

استخدم هذه الطريقة لتعبئة حقول دمج المراسلات في المستند بقيم من_ x000d_ صفيف من الكائنات.

تدمج هذه الطريقة البيانات لسجل واحد فقط. مصفوفة أسماء الحقول_ x000d_ ومجموعة القيم تمثل بيانات سجل واحد.

لا تستخدم هذه الطريقة مناطق دمج المراسلات.

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

### أمثلة

يوضح كيفية دمج صورة من URI كبيانات دمج البريد في MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs مع علامات "صورة:" ستتلقى صورة أثناء دمج المراسلات.
// السلسلة التي تلي علامة النقطتين في العلامة "صورة:" تتوافق مع اسم العمود
// في مصدر البيانات الذي تحتوي خلاياه على URIs لملفات الصور.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // إنشاء مصدر بيانات يحتوي على URIs للصور التي سنقوم بدمجها.
// يمكن أن يكون URI عنوان URL على الويب يشير إلى صورة ، أو اسم ملف نظام ملفات محلي لملف صورة.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// تنفيذ دمج البريد على مصدر بيانات بصف واحد.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

يوضح كيفية إجراء دمج المراسلات ، ثم حفظ المستند في مستعرض العميل.

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
    Throws.TypeOf<ArgumentNullException>()); // تم الإلقاء لأن HttpResponse فارغ في الاختبار.

// سنحتاج إلى إغلاق هذه الاستجابة يدويًا للتأكد من أننا لا نضيف أي محتوى غير ضروري إلى المستند بعد الحفظ.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### أنظر أيضا

* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

تنفيذ دمج المراسلات من DataTable في المستند.

```csharp
public void Execute(DataTable table)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| table | DataTable | الجدول الذي يحتوي على بيانات ليتم إدراجها في حقول دمج المراسلات. أسماء الحقول ليست حساسة لحالة الأحرف ._ x000d_ إذا تم العثور على اسم حقل غير موجود في المستند ، فسيتم تجاهله. |

### ملاحظات

استخدم هذه الطريقة لملء حقول دمج البريد في المستند بقيم من a  **جدول البيانات**.

يتم دمج كافة السجلات من الجدول في المستند.

يمكنك استخدام الحقل التالي في مستند Word للتسبب **دمج المراسلات** الكائن إلى select السجل التالي من ملف **جدول البيانات** ومتابعة الدمج . يمكن استخدام هذا عند إنشاء مستندات مثل الملصقات البريدية.

متي **دمج المراسلات**يصل الكائن إلى نهاية المستند الرئيسي ولا يزال هناك more من الصفوف في ملف **جدول البيانات**، يقوم بنسخ محتوى بالكامل من المستند الرئيسي وإلحاقه بنهاية المستند الوجهة باستخدام section break كفاصل.

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

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
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريد ناتج واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريد ناتج واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// ينشئ مستند مصدر لدمج المراسلات.
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

* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

تنفيذ دمج المراسلات من IDataReader في المستند.

```csharp
public void Execute(IDataReader dataReader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataReader | IDataReader | مصدر البيانات لعملية دمج المراسلات. |

### ملاحظات

يمكنك تمرير **SqlDataReader** أو **OleDbDataReader** الكائن في طريقة this كمعامل لأن كلاهما تم تنفيذهما **إداتاريدر** واجهه المستخدم.

لاحظ أن هذه الطريقة لا تستخدم مناطق دمج المراسلات وبالنسبة للسجلات المتعددة ، سيزداد حجم المستند x000d_ عن طريق تكرار المستند بأكمله.

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

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

// إنشاء سلسلة اتصال تشير إلى ملف قاعدة البيانات "Northwind"
// في نظام الملفات المحلي لدينا ، افتح اتصالاً ، وقم بإعداد استعلام SQL.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // أنشئ أمر SQL الذي سيصدر البيانات لدمج البريد الخاص بنا.
    // أسماء أعمدة الجدول التي سترجعها عبارة SELECT هذه
    // سيحتاج إلى أن يتوافق مع حقول الدمج التي وضعناها أعلاه.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // سيؤدي ذلك إلى تشغيل الأمر وتخزين البيانات في القارئ.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // خذ البيانات من القارئ واستخدمها في دمج البريد.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### أنظر أيضا

* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

تنفيذ دمج البريد من DataView في المستند.

```csharp
public void Execute(DataView dataView)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dataView | DataView | مصدر البيانات لعملية دمج المراسلات. |

### ملاحظات

هذه الطريقة مفيدة إذا قمت باسترداد البيانات إلى ملف **جدول البيانات** ولكن then تحتاج إلى تطبيق عامل تصفية أو فرز قبل دمج المراسلات.

لاحظ أن هذه الطريقة لا تستخدم مناطق دمج المراسلات وبالنسبة للسجلات المتعددة ، سيزداد حجم المستند x000d_ عن طريق تكرار المستند بأكمله.

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

### أمثلة

يوضح كيفية تحرير بيانات دمج البريد باستخدام DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// إنشاء جدول بيانات سيصدر منه دمج البريد البيانات.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// يمكننا استخدام طريقة عرض البيانات لتعديل بيانات دمج البريد دون إجراء تغييرات على جدول البيانات نفسه.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// يقوم عرض البيانات لدينا بفرز الإدخالات بترتيب تنازلي على طول عمود "الدرجة"
// وتصفية الصفوف بقيم أقل من 50 في هذا العمود.
// ثلاثة من الصفوف الأربعة تلائم هذه المعايير بحيث يحتوي مستند الإخراج على ثلاثة مستندات دمج.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### أنظر أيضا

* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

تنفيذ دمج المراسلات من DataRow في المستند.

```csharp
public void Execute(DataRow row)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| row | DataRow | الصف الذي يحتوي على بيانات لإدراجها في حقول دمج المراسلات. أسماء الحقول ليست حساسة لحالة الأحرف ._ x000d_ إذا تمت مصادفة اسم حقل غير موجود في المستند ، فسيتم تجاهله. |

### ملاحظات

استخدم هذه الطريقة لتعبئة حقول دمج المراسلات في المستند بقيم من ملف **داتاروو**.

هذه الطريقة تتجاهلRemoveUnusedRegions اختيار.

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
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريد ناتج واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريد ناتج واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// ينشئ مستند مصدر لدمج المراسلات.
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

* class [MailMerge](../../mailmerge)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
