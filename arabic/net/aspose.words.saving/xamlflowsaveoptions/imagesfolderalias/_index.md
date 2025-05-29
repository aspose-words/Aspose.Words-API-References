---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImagesFolderAlias في XamlFlowSaveOptions لتخصيص مسارات عناوين URI للصور في مستندات XAML. حسّن مشاريعك بسهولة!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند XAML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolderAlias { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق XAML، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.[`ImagesFolder`](../imagesfolder/) يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و`ImagesFolderAlias` يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

لو`ImagesFolderAlias` إذا لم تكن سلسلة فارغة، فإن عنوان URI للصورة الذي تمت كتابته إلى XAML سيكونImagesFolderAlias + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا كانت السلسلة فارغة، فإن عنوان URI للصورة المكتوبة إلى XAML سيكونمجلد الصور + &lt;اسم ملف الصورة&gt;.

لو`ImagesFolderAlias` إذا تم تعيينه على '.' (نقطة)، فسيتم كتابة اسم ملف الصورة إلى XAML بدون مسار بغض النظر عن الخيارات الأخرى.

## أمثلة

يوضح كيفية طباعة أسماء ملفات الصور المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى تنسيق .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // قم بإنشاء كائن "XamlFlowSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
    // لتعديل كيفية حفظ المستند إلى تنسيق الحفظ XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي الذي سيتم تخزين الصور فيه
    // سيقوم Aspose.Words بحفظ جميع الصور المرتبطة بالمستند.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الصور.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // يجب أن يحتوي المجلد المحدد بواسطة "ImagesFolderAlias" على الموارد بدلاً من "ImagesFolder".
    // يجب علينا التأكد من وجود المجلد قبل أن تتمكن تدفقات معاودة الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// يقوم بحساب وطباعة أسماء ملفات الصور أثناء تحويل مستندها الأصلي إلى صيغة .xaml.
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

        // إذا حددنا اسمًا مستعارًا لمجلد الصور، فسنحتاج أيضًا إلى
        //لإعادة توجيه كل تيار لوضع صورته في مجلد الاسم المستعار.
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
