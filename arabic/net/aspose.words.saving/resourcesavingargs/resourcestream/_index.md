---
title: ResourceSavingArgs.ResourceStream
linktitle: ResourceStream
articleTitle: ResourceStream
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ResourceSavingArgs ResourceStream لتحديد مكان حفظ مواردك بسهولة، مما يعزز الكفاءة والتحكم في مشاريعك.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcestream/
---
## ResourceSavingArgs.ResourceStream property

يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه.

```csharp
public Stream ResourceStream { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية حفظ الموارد في التدفقات بدلاً من الملفات.

القيمة الافتراضية هي`باطل` . عندما تكون هذه الخاصية`باطل` سيتم حفظ المورد في ملف محدد في[`ResourceFileName`](../resourcefilename/) ملكية.

استخدام[`IResourceSavingCallback`](../../iresourcesavingcallback/) لا يمكنك استبدال مورد بـ آخر. الغرض منه فقط هو التحكم في موقع حفظ الموارد.

## أمثلة

يوضح كيفية استخدام معاودة الاتصال لطباعة عناوين URI للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

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
    // يتعين علينا التأكد من وجود المجلد قبل أن تتمكن التدفقات من وضع مواردها فيه.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// يقوم بحساب وطباعة عناوين URI للموارد المضمنة أثناء تحويلها إلى HTML ثابت.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions، فسوف نتمكن من طباعته من هنا.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // بشكل افتراضي، يستخدم 'ResourceFileUri' مجلد النظام للخطوط.
                // لتجنب المشاكل في المنصات الأخرى، يجب عليك تحديد المسار للخطوط بشكل صريح.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // إذا قمنا بتحديد مجلد في خاصية "ResourcesFolderAlias"،
        // سوف نحتاج أيضًا إلى إعادة توجيه كل مجرى لوضع موارده في هذا المجلد.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
