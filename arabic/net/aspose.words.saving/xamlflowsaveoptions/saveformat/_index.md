---
title: XamlFlowSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveFormat في XamlFlowSaveOptions لحفظ مستنداتك بسهولة بتنسيق XamlFlow. حسّن سير عملك مع هذه الميزة الأساسية!
type: docs
weight: 60
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/saveformat/
---
## XamlFlowSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاXamlFlow .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
