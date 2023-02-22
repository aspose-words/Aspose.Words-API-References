---
title: XamlFlowSaveOptions.XamlFlowSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: XamlFlowSaveOptions البناء. يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقXamlFlow التنسيق .
type: docs
weight: 10
url: /ar/net/aspose.words.saving/xamlflowsaveoptions/xamlflowsaveoptions/
---
## XamlFlowSaveOptions() {#constructor}

يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقXamlFlow التنسيق .

```csharp
public XamlFlowSaveOptions()
```

### أمثلة

يوضح كيفية طباعة أسماء ملفات الصور المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى تنسيق .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // قم بإنشاء كائن "XamlFlowSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية حفظ المستند بتنسيق حفظ XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي فيه
    // Aspose.Words ستحفظ جميع الصور المرتبطة بالمستند.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الصور.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // سيحتاج المجلد المحدد بواسطة "ImagesFolderAlias" إلى احتواء الموارد بدلاً من "ImagesFolder".
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن تدفقات رد الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// يعد ويطبع أسماء ملفات الصور أثناء تحويل المستند الأصلي إلى نموذج تدفق .xaml.
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

        // إذا حددنا اسمًا مستعارًا لمجلد الصور ، فسنحتاج أيضًا إلى
        // لإعادة توجيه كل دفق لوضع صورته في مجلد الاسم المستعار.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### أنظر أيضا

* class [XamlFlowSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* المجسم [Aspose.Words](../../../)

---

## XamlFlowSaveOptions(SaveFormat) {#constructor_1}

يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقXamlFlow أوXamlFlowPack التنسيق .

```csharp
public XamlFlowSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن ان يكونXamlFlow أوXamlFlowPack. |

### أمثلة

يوضح كيفية طباعة أسماء ملفات الصور المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى تنسيق .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // قم بإنشاء كائن "XamlFlowSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية حفظ المستند بتنسيق حفظ XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي فيه
    // Aspose.Words ستحفظ جميع الصور المرتبطة بالمستند.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الصور.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // سيحتاج المجلد المحدد بواسطة "ImagesFolderAlias" إلى احتواء الموارد بدلاً من "ImagesFolder".
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن تدفقات رد الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// يعد ويطبع أسماء ملفات الصور أثناء تحويل المستند الأصلي إلى نموذج تدفق .xaml.
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

        // إذا حددنا اسمًا مستعارًا لمجلد الصور ، فسنحتاج أيضًا إلى
        // لإعادة توجيه كل دفق لوضع صورته في مجلد الاسم المستعار.
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
* مساحة الاسم [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* المجسم [Aspose.Words](../../../)


