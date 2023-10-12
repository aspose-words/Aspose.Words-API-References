---
title: SvgSaveOptions.ResourcesFolder
second_title: Aspose.Words لمراجع .NET API
description: SvgSaveOptions ملكية. يحدد المجلد الفعلي حيث يتم حفظ الموارد الصور عند تصدير مستند إلى تنسيق Svg. الافتراضي هوباطل .
type: docs
weight: 50
url: /ar/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور) عند تصدير مستند إلى تنسيق Svg. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolder { get; set; }
```

### ملاحظات

ليس له تأثير إلا إذا[`ExportEmbeddedImages`](../exportembeddedimages/) الملكية هي`خطأ شنيع`.

عندما تقوم بحفظ أ[`Document`](../../../aspose.words/document/) بتنسيق SVG، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ResourcesFolder` يسمح لك بتحديد مكان حفظ الصور و[`ResourcesFolderAlias`](../resourcesfolderalias/) يسمح بتحديد كيفية إنشاء معرفات URI للصورة.

إذا قمت بحفظ مستند في ملف وقمت بتوفير اسم ملف، فسيقوم Aspose.Words، افتراضيًا، بحفظ الصور في نفس المجلد حيث تم حفظ ملف المستند. يستخدم`ResourcesFolder` لتجاوز هذا السلوك.

إذا قمت بحفظ مستند في دفق، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ولكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في الملف`ResourcesFolder` ملكية

### أمثلة

يوضح كيفية معالجة وطباعة معرفات URI للموارد المرتبطة التي تم إنشاؤها أثناء تحويل مستند إلى .svg.

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
/// يحسب ويطبع عناوين URI للموارد الموجودة في الملف عند تحويلها إلى .svg.
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


