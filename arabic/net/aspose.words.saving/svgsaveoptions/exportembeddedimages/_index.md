---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تتيح لك خاصية SvgSaveOptions ExportEmbeddedImages تضمين الصور في ملفات SVG بتنسيق base64، مما يعزز قابلية النقل أثناء إدارة حجم الملف.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

يحدد ما إذا كان يجب تضمين الصور في مستند SVG بصيغة base64. انتبه إلى أن تنشيط هذا الخيار قد يؤدي إلى زيادة كبيرة في حجم ملف SVG الناتج.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## أمثلة

يوضح كيفية التعامل مع عناوين URI للموارد المرتبطة وطباعتها والتي تم إنشاؤها أثناء تحويل مستند إلى .svg.

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
/// يقوم بحساب وطباعة عناوين URI للموارد المضمنة بواسطة أثناء تحويلها إلى .svg.
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
