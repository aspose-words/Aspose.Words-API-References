---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words لـ .NET
description: ImageFieldMergingArgs Image ملكية. تحديد الصورة التي يجب على محرك دمج المراسلات إدراجها في المستند في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

تحديد الصورة التي يجب على محرك دمج المراسلات إدراجها في المستند.

```csharp
public Image Image { get; set; }
```

## أمثلة

يوضح كيفية استخدام رد الاتصال لتخصيص منطق دمج الصور.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // أدخل MERGEFIELD الذي سيقبل الصور من المصدر أثناء دمج البريد. استخدم رمز الحقل للرجوع إليه
    // عمود في مصدر البيانات يحتوي على أسماء ملفات النظام المحلي للصور التي نرغب في استخدامها في دمج البريد.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // في هذه الحالة، يتوقع الحقل أن يحتوي مصدر البيانات على عمود يسمى "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // يمكن أن تكون أسماء الملفات طويلة، وإذا تمكنا من إيجاد طريقة لتجنب تخزينها في مصدر البيانات،
    // قد نقوم بتقليل حجمه بشكل كبير.
    // قم بإنشاء مصدر بيانات يشير إلى الصور باستخدام الأسماء المختصرة.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // قم بتعيين رد اتصال مدمج يحتوي على كل المنطق الذي يعالج تلك الأسماء،
     // ثم قم بتنفيذ عملية دمج البريد.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// يحتوي على قاموس يقوم بتعيين أسماء الصور إلى أسماء ملفات النظام المحلي التي تحتوي على هذه الصور.
/// إذا كان مصدر بيانات دمج المراسلات يستخدم أحد أسماء القاموس للإشارة إلى صورة،
/// سوف يقوم رد الاتصال هذا بتمرير اسم الملف المعني إلى وجهة الدمج.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET48 || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### أنظر أيضا

* class [ImageFieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
