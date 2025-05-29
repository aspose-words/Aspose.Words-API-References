---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تسمح لك خاصية XamlFlowSaveOptions ImagesFolder بتحديد مجلد لحفظ الصور بسهولة عند تصدير المستندات إلى تنسيق XAML.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

يحدد المجلد الفعلي الذي يتم حفظ الصور فيه عند تصدير مستند إلى تنسيق XAML. الافتراضي هو سلسلة فارغة.

```csharp
public string ImagesFolder { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق XAML، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ImagesFolder` يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و[`ImagesFolderAlias`](../imagesfolderalias/) يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وأدخلت اسمًا للملف، فسيحفظ Aspose.Words افتراضيًا صور في نفس المجلد الذي حُفظ فيه ملف المستند. استخدم`ImagesFolder` لتجاوز هذا السلوك.

إذا حفظت مستندًا في مسار، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ، ولكنه سيحتاج إلى حفظ الصور في مكان ما. في هذه الحالة، ستحتاج إلى تحديد مجلد يمكن الوصول إليه في`ImagesFolder` الخاصية أو توفير تدفقات مخصصة عبر [`ImageSavingCallback`](../imagesavingcallback/) معالج الحدث.

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
