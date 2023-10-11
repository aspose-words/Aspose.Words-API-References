---
title: XamlFlowSaveOptions.ImageSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: XamlFlowSaveOptions ملكية. يسمح بالتحكم في كيفية حفظ الصور عند حفظ مستند في XAML.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/
---
## XamlFlowSaveOptions.ImageSavingCallback property

يسمح بالتحكم في كيفية حفظ الصور عند حفظ مستند في XAML.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

### أمثلة

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

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [XamlFlowSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* المجسم [Aspose.Words](../../../)


