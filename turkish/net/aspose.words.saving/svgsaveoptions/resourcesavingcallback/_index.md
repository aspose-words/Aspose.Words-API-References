---
title: SvgSaveOptions.ResourceSavingCallback
second_title: Aspose.Words for .NET API Referansı
description: SvgSaveOptions mülk. Bir belge SVG formatına dışa aktarıldığında kaynakların görüntülerin nasıl kaydedileceğini kontrol etmeyi sağlar.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Bir belge SVG formatına dışa aktarıldığında kaynakların (görüntülerin) nasıl kaydedileceğini kontrol etmeyi sağlar.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

### Örnekler

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
/// .svg'ye dönüştürüldükçe içerdiği kaynakların URI'lerini sayar ve yazdırır.
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
* ad alanı [Aspose.Words.Saving](../../svgsaveoptions/)
* toplantı [Aspose.Words](../../../)


