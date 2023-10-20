---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words لـ .NET
description: XamlFlowSaveOptions ImagesFolderAlias ملكية. يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند XAML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند XAML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

## ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق XAML، يحتاج Aspose.Words إلى حفظ كافة الصور المضمنة في المستند كملفات مستقلة.[`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد مكان حفظ الصور و`ImagesFolderAlias` يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

لو`ImagesFolderAlias` ليست سلسلة فارغة، فسيكون URI للصورة المكتوب إلى XAMLImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias`إذا كانت سلسلة فارغة، فسيكون URI للصورة المكتوبة إلى XAMLImagesFolder + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` تم ضبطه على "." (نقطة)، فسيتم كتابة اسم ملف الصورة إلى XAML بدون مسار بغض النظر عن الخيارات الأخرى.

## أمثلة

يوضح كيفية طباعة أسماء ملفات الصور المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى شكل تدفق .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // قم بإنشاء كائن "XamlFlowSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية حفظ المستند بتنسيق حفظ XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي الذي
    // Aspose.Words سيحفظ جميع الصور المرتبطة بالمستند.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء معرفات URI للصورة بدلاً من اسم مجلد الصور.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // المجلد المحدد بواسطة "ImagesFolderAlias" سيحتاج إلى أن يحتوي على الموارد بدلاً من "ImagesFolder".
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن تدفقات رد الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// يقوم بحساب وطباعة أسماء ملفات الصور أثناء تحويل المستند الأصلي إلى شكل انسيابي .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // إذا حددنا اسمًا مستعارًا لمجلد الصور، فسنحتاج أيضًا إلى ذلك
        // لإعادة توجيه كل تيار لوضع صورته في المجلد المستعار.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### أنظر أيضا

* class [XamlFlowSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
