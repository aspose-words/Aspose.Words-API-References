---
title: MergeFieldImageDimension.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MergeFieldImageDimension Value لتحسين معالجة الصور. حسّن مشروعك بأبعاد دقيقة وأداء مُحسّن.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/mergefieldimagedimension/value/
---
## MergeFieldImageDimension.Value property

القيمة.

```csharp
public double Value { get; set; }
```

## ملاحظات

يجب عليك استخدام قيمة سلبية للإشارة إلى أنه يجب تطبيق القيمة الأصلية لأبعاد الصورة المقابلة .

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

* class [MergeFieldImageDimension](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
