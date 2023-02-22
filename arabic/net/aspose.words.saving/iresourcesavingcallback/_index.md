---
title: Interface IResourceSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.IResourceSavingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ الموارد الخارجية الصور والخطوط و css عند حفظ مستند إلى صفحة ثابتة بتنسيق HTML أو SVG.
type: docs
weight: 4930
url: /ar/net/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ الموارد الخارجية (الصور والخطوط و css) عند حفظ مستند إلى صفحة ثابتة بتنسيق HTML أو SVG.

```csharp
public interface IResourceSavingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [ResourceSaving](../../aspose.words.saving/iresourcesavingcallback/resourcesaving/)(ResourceSavingArgs) | يتم الاستدعاء عند قيام Aspose.Words بحفظ مورد خارجي بتنسيق HTML أو SVG للصفحة الثابتة . |

### أمثلة

يوضح كيفية استخدام رد الاتصال لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// يتم الاستدعاء عندما يحفظ Aspose.Words موردًا خارجيًا لصفحة ثابتة HTML أو SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

يوضح كيفية استخدام رد اتصال لطباعة URIs للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

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
    // يجب أن نتأكد من وجود المجلد قبل أن تضع التدفقات مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// يحسب ويطبع URIs للموارد المتضمنة بواسطة حيث يتم تحويلها إلى HTML ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions ، فسنكون قادرين على طباعته من هنا.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // افتراضيًا ، يستخدم "ResourceFileUri" مجلد النظام للخطوط.
                // لتجنب المشاكل في الأنظمة الأساسية الأخرى ، يجب عليك تحديد مسار الخطوط بشكل صريح.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // إذا حددنا مجلدًا في خاصية "ResourcesFolderAlias" ،
        // سنحتاج أيضًا إلى إعادة توجيه كل دفق لوضع مورده في هذا المجلد.
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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


