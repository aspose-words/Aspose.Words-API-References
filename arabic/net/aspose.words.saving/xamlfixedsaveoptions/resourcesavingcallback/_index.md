---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words لـ .NET
description: XamlFixedSaveOptions ResourceSavingCallback ملكية. يسمح بالتحكم في كيفية حفظ الموارد الصور والخطوط عند تصدير مستند إلى تنسيق Xaml لصفحة ثابتة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

يسمح بالتحكم في كيفية حفظ الموارد (الصور والخطوط) عند تصدير مستند إلى تنسيق Xaml لصفحة ثابتة.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## أمثلة

يوضح كيفية طباعة معرفات URI للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى صيغة .xaml ذات النموذج الثابت.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // قم بإنشاء كائن "XamlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية حفظ المستند بتنسيق حفظ XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // استخدم خاصية "ResourcesFolder" لتعيين مجلد في نظام الملفات المحلي الذي
    // Aspose.Words سيحفظ جميع الموارد المرتبطة بالمستند، مثل الصور والخطوط.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // استخدم خاصية "ResourcesFolderAlias" لاستخدام هذا المجلد
    // عند إنشاء معرفات URI للصورة بدلاً من اسم مجلد الموارد.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // المجلد المحدد بواسطة "ResourcesFolderAlias" سيحتاج إلى أن يحتوي على الموارد بدلاً من "ResourcesFolder".
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن تدفقات رد الاتصال من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// يحسب ويطبع عناوين URI للموارد التي تم إنشاؤها أثناء التحويل إلى .xaml الثابت.
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

        // إذا حددنا اسمًا مستعارًا لمجلد المورد، فسنحتاج إليه أيضًا
        // لإعادة توجيه كل تيار لوضع موارده في المجلد المستعار.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### أنظر أيضا

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
