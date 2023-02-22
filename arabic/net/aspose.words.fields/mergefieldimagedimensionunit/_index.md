---
title: Enum MergeFieldImageDimensionUnit
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.MergeFieldImageDimensionUnit تعداد. يحدد وحدة أبعاد الصورة أي العرض أو الارتفاع المستخدمة عبر عملية دمج البريد.
type: docs
weight: 2580
url: /ar/net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

يحدد وحدة أبعاد الصورة (أي العرض أو الارتفاع) المستخدمة عبر عملية دمج البريد.

```csharp
public enum MergeFieldImageDimensionUnit
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Point | `0` | النقطة (أي 1/72 بوصة) . |
| Percent | `1` | النسبة المئوية لقيمة أبعاد الصورة الأصلية . |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


