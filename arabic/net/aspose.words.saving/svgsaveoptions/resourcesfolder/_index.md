---
title: SvgSaveOptions.ResourcesFolder
second_title: Aspose.Words لمراجع .NET API
description: SvgSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الموارد الصور عند تصدير مستند إلى تنسيق Svg . الافتراضي هولا شيء .
type: docs
weight: 50
url: /ar/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور) عند تصدير مستند إلى تنسيق Svg . الافتراضي هو`لا شيء` .

```csharp
public string ResourcesFolder { get; set; }
```

### ملاحظات

له تأثير فقط إذا[`ExportEmbeddedImages`](../exportembeddedimages/) الملكية خاطئة.

عندما تقوم بحفظ ملف[`Document`](../../../aspose.words/document/)بتنسيق SVG ، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات قائمة بذاتها.`ResourcesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ResourcesFolderAlias`](../resourcesfolderalias/) يسمح بتحديد كيفية إنشاء عناوين URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف ، Aspose.Words ، بشكل افتراضي ، يحفظ الصور في نفس المجلد حيث يتم حفظ ملف المستند. يستخدم`ResourcesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق ، فإن Aspose.Words ليس بها مجلد لحفظ الصور ، ولكن لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة ، تحتاج إلى تحديد مجلد يمكن الوصول إليه في ملف`ResourcesFolder` منشأه

### أمثلة

يوضح كيفية معالجة وطباعة URIs للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// يحسب ويطبع URIs للموارد المتضمنة بواسطة عندما يتم تحويلها إلى .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../svgsaveoptions/)
* المجسم [Aspose.Words](../../../)


