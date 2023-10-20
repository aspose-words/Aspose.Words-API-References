---
title: HtmlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words لـ .NET
description: HtmlFixedSaveOptions ResourcesFolder ملكية. يحدد المجلد الفعلي حيث يتم حفظ الموارد الصور الخطوط CSS عند تصدير مستند إلى تنسيق Html. الافتراضي هوباطل  في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور، الخطوط، CSS) عند تصدير مستند إلى تنسيق Html. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolder { get; set; }
```

## ملاحظات

ليس له تأثير إلا إذا[`ExportEmbeddedImages`](../exportembeddedimages/) الملكية هي`خطأ شنيع`.

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق Html، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ResourcesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ResourcesFolderAlias`](../resourcesfolderalias/) يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فسيقوم Aspose.Words، افتراضيًا، بحفظ الصور في نفس المجلد حيث تم حفظ ملف المستند. يستخدم`ResourcesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه باستخدام الملف`ResourcesFolder` ملكية

## أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
