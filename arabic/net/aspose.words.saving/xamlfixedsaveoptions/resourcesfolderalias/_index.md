---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ResourcesFolderAlias في XamlFixedSaveOptions إدارة عناوين URI للصور في مستندات Xaml. حسّن تخطيطات صفحاتك الثابتة اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند Xaml ذي الصفحة الثابتة. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## ملاحظات

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق Xaml للصفحة الثابتة، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.[`ResourcesFolder`](../resourcesfolder/) يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و`ResourcesFolderAlias` يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

## أمثلة

يوضح كيفية طباعة عناوين URI للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى نموذج ثابت من .xaml.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // قم بإنشاء كائن "XamlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية حفظ المستند إلى تنسيق الحفظ XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // استخدم خاصية "ResourcesFolder" لتعيين مجلد في نظام الملفات المحلي الذي سيتم تخزين الموارد فيه
    // سيقوم Aspose.Words بحفظ جميع الموارد المرتبطة بالمستند، مثل الصور والخطوط.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // استخدم خاصية "ResourcesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الموارد.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // يجب أن يحتوي المجلد المحدد بواسطة "ResourcesFolderAlias" على الموارد بدلاً من "ResourcesFolder".
    // يجب علينا التأكد من وجود المجلد قبل أن تتمكن تدفقات معاودة الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// يقوم بحساب وطباعة عناوين URI للموارد التي تم إنشاؤها أثناء التحويل إلى .xaml الثابتة.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // إذا حددنا اسمًا مستعارًا لمجلد الموارد، فسنحتاج أيضًا إلى
        //لإعادة توجيه كل مجرى لوضع موارده في مجلد الاسم المستعار.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### أنظر أيضا

* class [XamlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
