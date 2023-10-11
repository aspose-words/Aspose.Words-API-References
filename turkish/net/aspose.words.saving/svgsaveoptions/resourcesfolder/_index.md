---
title: SvgSaveOptions.ResourcesFolder
second_title: Aspose.Words for .NET API Referansı
description: SvgSaveOptions mülk. Bir belge Svg formatında dışa aktarılırken kaynakların görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılanhükümsüz .
type: docs
weight: 50
url: /tr/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Bir belge Svg formatında dışa aktarılırken kaynakların (görüntülerin) kaydedildiği fiziksel klasörü belirtir. Varsayılan:`hükümsüz` .

```csharp
public string ResourcesFolder { get; set; }
```

### Notlar

Yalnızca şu durumlarda etkilidir:[`ExportEmbeddedImages`](../exportembeddedimages/) mülkiyet`YANLIŞ`.

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) SVG formatında Aspose.Words'ün belgeye gömülü all görüntülerini bağımsız dosyalar olarak kaydetmesi gerekir.`ResourcesFolder` görüntülerin nereye kaydedileceğini belirtmenize ve[`ResourcesFolderAlias`](../resourcesfolderalias/) , görüntü URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntülerini belge dosyasının kaydedildiği klasöre kaydeder. Kullanmak`ResourcesFolder` Bu davranışı geçersiz kılmak için .

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'de görüntülerin kaydedileceği bir klasör yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir.`ResourcesFolder` mülk

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

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../svgsaveoptions/)
* toplantı [Aspose.Words](../../../)


