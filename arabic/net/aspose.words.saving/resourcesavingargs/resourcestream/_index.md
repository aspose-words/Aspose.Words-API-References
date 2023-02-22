---
title: ResourceSavingArgs.ResourceStream
second_title: Aspose.Words لمراجع .NET API
description: ResourceSavingArgs ملكية. يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcestream/
---
## ResourceSavingArgs.ResourceStream property

يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه.

```csharp
public Stream ResourceStream { get; set; }
```

### ملاحظات

تسمح لك هذه الخاصية بحفظ الموارد في التدفقات بدلاً من الملفات.

النظام الأساسي`لا شيء` . عندما تكون هذه الخاصية`لا شيء` ، سيتم حفظ المورد في ملف محدد في[`ResourceFileName`](../resourcefilename/) منشأه.

استخدام[`IResourceSavingCallback`](../../iresourcesavingcallback/) لا يمكنك استبدال مورد بـ آخر. الغرض منه هو فقط التحكم في الموقع حيث يتم حفظ الموارد.

### أمثلة

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

* class [ResourceSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../resourcesavingargs/)
* المجسم [Aspose.Words](../../../)


