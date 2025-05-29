---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: .NET için Aspose.Words
description: SvgSaveOptions ExportEmbeddedImages özelliğinin, dosyaları base64 olarak SVG dosyalarına gömerek taşınabilirliği artırırken dosya boyutunu yönetmenizi nasıl sağladığını keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Görüntülerin SVG belgesine base64 olarak gömülmesi gerekip gerekmediğini belirtir. Bu seçeneğin etkinleştirilmesinin çıktı SVG dosyasının boyutunda önemli bir artışa yol açabileceğini unutmayın.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Örnekler

Bir belgeyi .svg'ye dönüştürürken oluşturulan bağlantılı kaynakların URI'lerinin nasıl düzenleneceğini ve yazdırılacağını gösterir.

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
/// .svg'ye dönüştürülürken, içerdiği kaynakların URI'lerini sayar ve yazdırır.
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

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
