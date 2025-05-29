---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: Aspose.Words لـ .NET
description: قم بضبط ImageWidth في ImageFieldMergingArgs لإدراج الصور بسلاسة في مستنداتك، مما يعزز الجاذبية البصرية والتخطيط.
type: docs
weight: 50
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

يحدد عرض الصورة التي سيتم إدراجها في المستند.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## ملاحظات

تأتي قيمة هذه الخاصية مبدئيًا من كود MERGEFIELD المقابل، الموجود في مستند القالب . لتجاوز القيمة الأولية، يجب عليك تعيين مثيل لـ [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) الفئة لهذه الخاصية أو تعيين الخصائص لـ instance من[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) الفئة التي تم إرجاعها بواسطة هذه الخاصية.

للإشارة إلى أنه يجب تطبيق القيمة الأصلية لعرض الصورة، يجب عليك تعيين`باطل` القيمة لهذه الخاصية أو تعيين[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) خاصية لـ instance من[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) الفئة التي تم إرجاعها بواسطة هذه الخاصية إلى قيمة سلبية.

## أمثلة

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

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
