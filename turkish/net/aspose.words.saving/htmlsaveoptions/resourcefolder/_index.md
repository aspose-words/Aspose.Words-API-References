---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: .NET için Aspose.Words
description: En iyi belge dışa aktarımı için HtmlSaveOptions ResourceFolder özelliğini keşfedin. Belirlenen bir klasördeki görüntüleri, yazı tiplerini ve CSS'yi kolayca yönetin.
type: docs
weight: 440
url: /tr/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Bir belge HTML'ye aktarıldığında, resimler, yazı tipleri ve harici CSS gibi tüm kaynakların kaydedildiği fiziksel bir klasörü belirtir. Varsayılan boş bir dizedir.

```csharp
public string ResourceFolder { get; set; }
```

## Notlar

`ResourceFolder` tüm kaynakların yazılacağı klasörü belirtmenin en basit yoludur. Başka bir yol da bireysel özellikleri kullanmaktır[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , ve[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` belirtilen klasörlerden daha düşük önceliğe sahiptir[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , Ve[`CssStyleSheetFileName`](../cssstylesheetfilename/) Örneğin, her ikisi de ise`ResourceFolder` Ve[`FontsFolder`](../fontsfolder/)belirtildiğinde, yazı tipleri kaydedilecek [`FontsFolder`](../fontsfolder/) , resimler ve CSS kaydedilirken`ResourceFolder`.

Belirtilen klasör`ResourceFolder` mevcut değilse, otomatik olarak oluşturulacaktır.

## Örnekler

Aspose.Words'ün bir belgeyi HTML'e kaydederken oluşturacağı harici olarak kaydedilen kaynaklar için klasörlerin ve klasör takma adlarının nasıl ayarlanacağını gösterir.

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
    FontsFolderAlias = "http://example.com/yazı tipleri",
    ImagesFolderAlias = "http://example.com/resimler",
    ResourceFolderAlias = "http://example.com/kaynaklar",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
