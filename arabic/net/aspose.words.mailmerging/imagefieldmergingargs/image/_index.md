---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام ImageFieldMergingArgs لإدراج الصور بسلاسة في مستنداتك للحصول على تجربة دمج بريد مصقولة.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند.

```csharp
public Image Image { get; set; }
```

## أمثلة

يوضح كيفية استخدام معاودة الاتصال لتخصيص منطق دمج الصور.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // أدخل حقل دمج يقبل الصور من مصدر أثناء دمج البريد. استخدم رمز الحقل للإشارة إليه.
    // عمود في مصدر البيانات يحتوي على أسماء ملفات النظام المحلي للصور التي نرغب في استخدامها في دمج البريد.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // في هذه الحالة، يتوقع الحقل أن يحتوي مصدر البيانات على عمود يسمى "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // يمكن أن تكون أسماء الملفات طويلة، وإذا تمكنا من إيجاد طريقة لتجنب تخزينها في مصدر البيانات،
    //قد نتمكن من تقليص حجمها بشكل كبير.
    // إنشاء مصدر بيانات يشير إلى الصور باستخدام أسماء قصيرة.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // تعيين استدعاء دمج يحتوي على كل المنطق الذي يعالج تلك الأسماء،
     //ثم قم بتنفيذ دمج البريد.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// يحتوي على قاموس يربط أسماء الصور بأسماء ملفات النظام المحلي التي تحتوي على هذه الصور.
/// إذا كان مصدر بيانات دمج البريد يستخدم أحد أسماء القاموس للإشارة إلى صورة،
/// ستمرر هذه الدالة الراجعة اسم الملف المعني إلى وجهة الدمج.
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
            #if NET461_OR_GREATER || JAVA
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
