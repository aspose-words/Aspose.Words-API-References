---
title: SvgSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words لمراجع .NET API
description: SvgSaveOptions ملكية. تم تحديد ما إذا كان يجب تضمين الصور في مستند SVG كـ base64. ملاحظة يمكن أن يؤدي تعيين هذه العلامة إلى زيادة حجم ملف SVG الناتج بشكل ملحوظ.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

تم تحديد ما إذا كان يجب تضمين الصور في مستند SVG كـ base64. ملاحظة يمكن أن يؤدي تعيين هذه العلامة إلى زيادة حجم ملف SVG الناتج بشكل ملحوظ.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

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


