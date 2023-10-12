---
title: HtmlFixedSaveOptions.ResourcesFolderAlias
second_title: Aspose.Words لمراجع .NET API
description: HtmlFixedSaveOptions ملكية. يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند Html. الافتراضي هوباطل .
type: docs
weight: 150
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/
---
## HtmlFixedSaveOptions.ResourcesFolderAlias property

يحدد اسم المجلد المستخدم لإنشاء معرفات URI للصور المكتوبة في مستند Html. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

### ملاحظات

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق Html، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.[`ResourcesFolder`](../resourcesfolder/) يسمح لك بتحديد مكان حفظ الصور و`ResourcesFolderAlias` يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

### أمثلة

يوضح كيفية استخدام رد اتصال لطباعة معرفات URI للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // سيحتوي المجلد المحدد بواسطة ResourcesFolderAlias على الموارد بدلاً من ResourcesFolder.
    // يجب أن نتأكد من وجود المجلد قبل أن تتمكن التدفقات من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// يحسب ويطبع عناوين URI للموارد التي تحتوي عليها عند تحويلها إلى HTML ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions، فسنكون قادرين على طباعته من هنا.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // بشكل افتراضي، يستخدم 'ResourceFileUri' مجلد النظام للخطوط.
                // لتجنب المشاكل في الأنظمة الأساسية الأخرى، يجب عليك تحديد مسار الخطوط بشكل صريح.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // إذا قمنا بتحديد مجلد في خاصية "ResourcesFolderAlias"،
        // سنحتاج أيضًا إلى إعادة توجيه كل تيار لوضع موارده في هذا المجلد.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


