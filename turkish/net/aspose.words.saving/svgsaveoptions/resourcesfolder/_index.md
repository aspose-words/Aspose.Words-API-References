---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: .NET için Aspose.Words
description: Belgeleri SVG formatına aktarırken verimli görüntü depolama için SvgSaveOptions'da ResourcesFolder'ı nasıl ayarlayacağınızı keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 80
url: /tr/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Bir belgeyi Svg biçimine aktarırken kaynakların (görüntülerin) kaydedildiği fiziksel klasörü belirtir. Varsayılan`hükümsüz` .

```csharp
public string ResourcesFolder { get; set; }
```

## Notlar

Yalnızca şu durumlarda etkilidir:[`ExportEmbeddedImages`](../exportembeddedimages/) mülkiyet`YANLIŞ`.

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) SVG formatında, Aspose.Words'ün belgeye gömülü tüm resimleri bağımsız dosyalar olarak kaydetmesi gerekir.`ResourcesFolder` görüntülerin nereye kaydedileceğini belirtmenize olanak tanır ve[`ResourcesFolderAlias`](../resourcesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmeye izin verir.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak, resimlerini belge dosyasının kaydedildiği klasöre kaydeder.`ResourcesFolder` Bu davranışı geçersiz kılmak için kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'ün görüntüleri kaydedeceği bir klasörü yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir`ResourcesFolder` mülk

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
