---
title: ImageFieldMergingArgs.ImageHeight
linktitle: ImageHeight
articleTitle: ImageHeight
second_title: Aspose.Words لـ .NET
description: ImageFieldMergingArgs ImageHeight ملكية. يحدد ارتفاع الصورة المراد إدراجها في المستند في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/imageheight/
---
## ImageFieldMergingArgs.ImageHeight property

يحدد ارتفاع الصورة المراد إدراجها في المستند.

```csharp
public MergeFieldImageDimension ImageHeight { get; set; }
```

## ملاحظات

تأتي قيمة هذه الخاصية في البداية من كود MERGEFIELD المطابق، الموجود في مستند قالب . لتجاوز القيمة الأولية، يجب عليك تعيين مثيل of [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) فئة لهذه الخاصية أو قم بتعيين خصائص المثيل of[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) فئة تم إرجاعها بواسطة هذه الخاصية.

للإشارة إلى ضرورة تطبيق القيمة الأصلية لارتفاع الصورة، يجب عليك تعيين`باطل` قيمة لهذه الخاصية أو قم بتعيين القيمة[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) خاصية المثيل of[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) الفئة التي تم إرجاعها بواسطة هذه الخاصية إلى قيمة سالبة.

## أمثلة

يوضح كيفية تعيين أبعاد الصور كما يقبلها MERGEFIELDS أثناء دمج البريد.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // أدخل MERGEFIELD الذي سيقبل الصور من المصدر أثناء دمج البريد. استخدم رمز الحقل للرجوع إليه
    // عمود في مصدر البيانات يحتوي على أسماء ملفات النظام المحلي للصور التي نرغب في استخدامها في دمج البريد.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // يجب أن يحتوي مصدر البيانات على عمود يسمى "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // قم بإنشاء مصدر بيانات مناسب.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // قم بتكوين رد اتصال لتعديل أحجام الصور في وقت الدمج، ثم قم بتنفيذ عملية دمج البريد.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// يضبط حجم جميع الصور المدمجة بالبريد على عرض وارتفاع محددين.
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

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
