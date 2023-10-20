---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words لـ .NET
description: SvgSaveOptions ExportEmbeddedImages ملكية. تحديد ما إذا كان يجب تضمين الصور في مستند SVG كأساس 64. ملاحظة يمكن أن يؤدي تعيين هذه العلامة إلى زيادة حجم ملف SVG الناتج بشكل ملحوظ في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

تحديد ما إذا كان يجب تضمين الصور في مستند SVG كأساس 64. ملاحظة: يمكن أن يؤدي تعيين هذه العلامة إلى زيادة حجم ملف SVG الناتج بشكل ملحوظ.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
