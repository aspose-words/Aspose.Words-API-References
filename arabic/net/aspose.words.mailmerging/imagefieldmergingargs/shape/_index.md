---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية Shape الخاصة بـ ImageFieldMergingArgs على تحسين مستندات دمج البريد الخاصة بك من خلال السماح بإدراج الشكل بدقة للحصول على مظهر أنيق.
type: docs
weight: 60
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند.

```csharp
public Shape Shape { get; set; }
```

## ملاحظات

عند تحديد هذه الخاصية، يتجاهل محرك دمج البريد جميع الخصائص الأخرى مثل[`ImageFileName`](../imagefilename/) أو[`ImageStream`](../imagestream/) ويقوم ببساطة بإدراج الشكل في المستند.

استخدم هذه الخاصية للتحكم الكامل في عملية دمج حقل دمج الصور. على سبيل المثال، يمكنك تحديد[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/)أو أي خاصية شكل أخرى لضبط العقدة الناتجة. مع ذلك، يُرجى ملاحظة أنك مسؤول عن توفير محتوى الشكل.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
