---
title: XamlFixedSaveOptions.ResourcesFolder
second_title: Aspose.Words لمراجع .NET API
description: XamlFixedSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الموارد الصور والخطوط عند تصدير مستند إلى تنسيق Xaml لصفحة ثابتة. الافتراضي هوباطل .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور والخطوط) عند تصدير مستند إلى تنسيق Xaml لصفحة ثابتة. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolder { get; set; }
```

### ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) في تنسيق Xaml للصفحة الثابتة، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ResourcesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ResourcesFolderAlias`](../resourcesfolderalias/) يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فسيقوم Aspose.Words، افتراضيًا، بحفظ الصور في نفس المجلد حيث تم حفظ ملف المستند. يستخدم`ResourcesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه باستخدام الملف`ResourcesFolder` ملكية

### أمثلة

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

* class [XamlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xamlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


