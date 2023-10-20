---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ResourceFolder mülk. Bir document HTMLye aktarıldığında görüntüler yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir C#'da.
type: docs
weight: 420
url: /tr/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Bir document HTML'ye aktarıldığında görüntüler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir.

```csharp
public string ResourceFolder { get; set; }
```

## Notlar

`ResourceFolder` tüm kaynakların yazılması gereken klasörü belirtmenin en basit yoludur. Diğer bir yol ise bireysel özellikleri kullanmaktır[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , ve[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` aracılığıyla belirtilen klasörlerden daha düşük önceliğe sahiptir[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , Ve[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Örneğin, eğer her ikisi de `ResourceFolder` Ve[`FontsFolder`](../fontsfolder/)belirtildiğinde yazı tipleri kaydedilecek [`FontsFolder`](../fontsfolder/) , resimler ve CSS ise şuraya kaydedilecek:`ResourceFolder`.

tarafından belirtilen klasör ise`ResourceFolder` mevcut değil, otomatik olarak oluşturulacak.

## Örnekler

Aspose.Words'ün bir belgeyi HTML'ye kaydederken oluşturacağı harici olarak kaydedilen kaynaklar için klasörlerin ve klasör takma adlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
