---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: .NET için Aspose.Words
description: Bağlantılı resimler için orijinal URL'ler kullanmanıza olanak tanıyan HtmlSaveOptions' ExportOriginalUrlForLinkedImages özelliğini keşfedin. Belgenizin bütünlüğünü artırın!
type: docs
weight: 200
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Bağlantılı resimlerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Notlar

Değer olarak ayarlanırsa`doğru`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) değer, bağlantılı resimlerin URL'si olarak kullanılır ve bağlantılı resimler belgenin klasörüne yüklenmez veya[`ImagesFolder`](../imagesfolder/).

Değer olarak ayarlanırsa`YANLIŞ`bağlantılı resimler belgenin klasörüne yüklenir veya[`ImagesFolder`](../imagesfolder/) ve her bağlantılı görüntünün URL'si, belgenin klasörüne bağlı olarak oluşturulur,[`ImagesFolder`](../imagesfolder/) ve[`ImagesFolderAlias`](../imagesfolderalias/) özellikler.

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
