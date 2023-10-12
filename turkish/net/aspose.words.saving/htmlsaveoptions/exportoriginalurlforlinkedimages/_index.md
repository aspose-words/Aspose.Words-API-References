---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Bağlantılı görsellerin URLsi olarak orijinal URLnin kullanılıp kullanılmayacağını belirtir. Varsayılan değerYANLIŞ .
type: docs
weight: 200
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Bağlantılı görsellerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

### Notlar

Değer olarak ayarlanmışsa`doğru`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) Bağlantılı görsellerin URL'si ve bağlantılı görseller belgenin klasörüne yüklenmediğinden değer use şeklindedir veya[`ImagesFolder`](../imagesfolder/).

Değer olarak ayarlanmışsa`YANLIŞ`bağlantılı resimler belgenin klasörüne veya yüklenir[`ImagesFolder`](../imagesfolder/) ve bağlantılı her görüntünün URL'si, belgenin klasörüne bağlı olarak oluşturulur,[`ImagesFolder`](../imagesfolder/) ve[`ImagesFolderAlias`](../imagesfolderalias/) özellikler.

### Örnekler

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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


