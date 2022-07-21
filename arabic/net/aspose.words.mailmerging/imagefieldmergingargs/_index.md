---
title: ImageFieldMergingArgs
second_title: Aspose.Words لمراجع .NET API
description: توفير بيانات لملفImageFieldMerging./ifieldmergingcallback/imagefieldmerging الحدث .
type: docs
weight: 3610
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

توفير بيانات لملف[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging) الحدث .

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document) { get; } | إرجاع ملف[`Document`](../fieldmergingargsbase/document) الكائن الذي يتم تنفيذ دمج المراسلات. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname) { get; } | الحصول على اسم حقل الدمج كما هو محدد في المستند. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field) { get; } | الحصول على الكائن الذي يمثل حقل الدمج الحالي. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname) { get; } | الحصول على اسم حقل الدمج في مصدر البيانات. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue) { get; set; } | الحصول على أو تعيين قيمة الحقل من مصدر البيانات. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image) { get; set; } | يحدد الصورة التي يجب على محرك دمج المراسلات إدراجها في المستند. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename) { get; set; } | يعيّن اسم ملف الصورة الذي يجب على محرك دمج المراسلات إدراجه في المستند. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight) { get; set; } | يحدد ارتفاع الصورة للصورة لإدراجها في المستند. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream) { get; set; } | تحديد دفق محرك دمج المراسلات لقراءة صورة منه. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth) { get; set; } | يحدد عرض الصورة للصورة لإدراجها في المستند. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex) { get; } | الحصول على فهرس السجل الذي يتم دمجه على أساس الصفر. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape) { get; set; } | تحديد الشكل الذي يجب على محرك دمج المراسلات إدراجه في المستند. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename) { get; } | الحصول على اسم جدول البيانات لعملية الدمج الحالية أو السلسلة الفارغة إذا لم يكن الاسم متاحًا . |

### ملاحظات

يحدث هذا الحدث أثناء دمج المراسلات عند مصادفة حقل merge بريد صورة في المستند. يمكنك الرد على هذا الحدث لإرجاع اسم ملف أو دفق أو ملفImage الكائن إلى محرك merge mailge بحيث يتم إدراجه في المستند.

هناك ثلاث خصائص متاحة[`ImageFileName`](./imagefilename) ، [`ImageStream`](./imagestream) و[`Image`](./image) لتحديد المكان الذي يجب أن تؤخذ منه الصورة. قم بتعيين واحدة فقط من هذه الخصائص.

لإدراج حقل دمج بريد صورة في مستند في Word ، حدد أمر إدراج / حقل ، ثم حدد MergeField واكتب Image: MyFieldName.

### أمثلة

يوضح كيفية إدراج الصور المخزنة في حقل BLOB لقاعدة البيانات في تقرير.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // افتح قارئ البيانات ، الذي يجب أن يكون في وضع يقرأ جميع السجلات مرة واحدة.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج المراسلات MERGEFIELD في المستند بعلامة "صورة:" في اسمه.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

يوضح كيفية تعيين أبعاد الصور حيث تقبلها MERGEFIELDS أثناء دمج البريد.

```csharp
{
    Document doc = new Document();

    // أدخل MERGEFIELD الذي سيقبل الصور من مصدر أثناء دمج البريد. استخدم رمز الحقل للرجوع إليه
    // عمود في مصدر البيانات يحتوي على أسماء ملفات النظام المحلي للصور التي نرغب في استخدامها في دمج البريد.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // يجب أن يحتوي مصدر البيانات على عمود يسمى "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // إنشاء مصدر بيانات مناسب.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // تكوين رد اتصال لتعديل أحجام الصور في وقت الدمج ، ثم تنفيذ دمج البريد.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// يعين حجم كل الصور المدمجة في البريد على عرض وارتفاع محددين.
/// </summary>
private class MergedImageResizer : IFieldMergingCallback
{
    public MergedImageResizer(double imageWidth, double imageHeight, MergeFieldImageDimensionUnit unit)
    {
        mImageWidth = imageWidth;
        mImageHeight = imageHeight;
        mUnit = unit;
    }

    public void FieldMerging(FieldMergingArgs e)
    {
        throw new NotImplementedException();
    }

    public void ImageFieldMerging(ImageFieldMergingArgs args)
    {
        args.ImageFileName = args.FieldValue.ToString();
        args.ImageWidth = new MergeFieldImageDimension(mImageWidth, mUnit);
        args.ImageHeight = new MergeFieldImageDimension(mImageHeight, mUnit);

        Assert.AreEqual(mImageWidth, args.ImageWidth.Value);
        Assert.AreEqual(mUnit, args.ImageWidth.Unit);
        Assert.AreEqual(mImageHeight, args.ImageHeight.Value);
        Assert.AreEqual(mUnit, args.ImageHeight.Unit);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### أنظر أيضا

* class [FieldMergingArgsBase](../fieldmergingargsbase)
* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
