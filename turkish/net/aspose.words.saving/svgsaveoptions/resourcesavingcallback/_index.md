---
title: SvgSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words for .NET
description: SvgSaveOptions ResourceSavingCallback mülk. Bir belge SVG formatında dışa aktarıldığında kaynakların görüntülerin nasıl kaydedildiğini kontrol etmeye olanak tanır C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Bir belge SVG formatında dışa aktarıldığında kaynakların (görüntülerin) nasıl kaydedildiğini kontrol etmeye olanak tanır.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## Örnekler

Bir belgeyi .svg'ye dönüştürürken oluşturulan bağlantılı kaynakların URI'lerinin nasıl değiştirileceğini ve yazdırılacağını gösterir.

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
/// .svg'ye dönüştürülürken içerdiği kaynakların URI'lerini sayar ve yazdırır.
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

### Ayrıca bakınız

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
