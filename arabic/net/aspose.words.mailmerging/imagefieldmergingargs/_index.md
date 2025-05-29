---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMerging.ImageFieldMergingArgs، المصممة لتحسين دمج الصور في المستندات، مما يضمن سير عمل سلس وفعال.
type: docs
weight: 4520
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

يوفر بيانات لـ[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) الحدث.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | يعيد[`Document`](../fieldmergingargsbase/document/)الكائن الذي يتم تنفيذ عملية دمج البريد له. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | يحصل على اسم حقل الدمج كما هو محدد في المستند. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | يحصل على الكائن الذي يمثل حقل الدمج الحالي. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | يحصل على اسم حقل الدمج في مصدر البيانات. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | يحصل على قيمة الحقل من مصدر البيانات أو يعينها. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | يحدد اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | يحدد ارتفاع الصورة التي سيتم إدراجها في المستند. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | يحدد التدفق الذي سيقرأ منه محرك دمج البريد صورة. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | يحدد عرض الصورة التي سيتم إدراجها في المستند. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | يحصل على الفهرس الصفري للسجل الذي يتم دمجه. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا لم يكن الاسم متاحًا. |

## ملاحظات

يحدث هذا الحدث أثناء دمج البريد عند وجود حقل دمج بريدي للصورة في المستند. يمكنك الاستجابة لهذا الحدث لإرجاع اسم ملف أو دفق أوImage قم بدمج الكائن في محرك الدمج البريدي حتى يتم إدراجه في المستند.

هناك ثلاث خصائص متاحة[`ImageFileName`](./imagefilename/) ، [`ImageStream`](./imagestream/) و[`Image`](./image/) لتحديد المكان الذي يجب التقاط الصورة منه. قم بتعيين إحدى هذه الخصائص فقط.

لإدراج حقل دمج بريدي للصورة في مستند في Word، حدد أمر الإدراج/الحقل، ثم حدد MergeField واكتب Image:MyFieldName.

## أمثلة

يوضح كيفية إدراج الصور المخزنة في حقل BLOB بقاعدة البيانات في تقرير.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // افتح قارئ البيانات، والذي يجب أن يكون في وضع يقرأ جميع السجلات مرة واحدة.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        //لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج البريد MERGEFIELD في المستند مع علامة "Image:" في اسمه.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

يوضح كيفية تعيين أبعاد الصور كما يقبلها MERGEFIELDS أثناء دمج البريد.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // أدخل حقل دمج يقبل الصور من مصدر أثناء دمج البريد. استخدم رمز الحقل للإشارة إليه.
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

    // قم بتكوين معاودة الاتصال لتعديل أحجام الصور في وقت الدمج، ثم قم بتنفيذ دمج البريد.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// تعيين حجم جميع الصور المدمجة بالبريد إلى عرض وارتفاع محددين.
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
        Assert.Null(args.Shape);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### أنظر أيضا

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
