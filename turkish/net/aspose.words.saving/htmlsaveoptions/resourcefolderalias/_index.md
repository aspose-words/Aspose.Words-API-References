---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: .NET için Aspose.Words
description: Kaynakların URI olarak verimli bir şekilde oluşturulması için klasör adlarını tanımlayan HtmlSaveOptions ResourceFolderAlias özelliğiyle HTML belgelerinizi optimize edin.
type: docs
weight: 450
url: /tr/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Bir HTML belgesine yazılan tüm kaynakların URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Notlar

`ResourceFolderAlias` tüm kaynak dosyaları için URI'lerin nasıl oluşturulacağını belirtmenin en basit yoludur . Aynı bilgiler, resimler ve yazı tipleri için ayrı ayrı belirtilebilir[`ImagesFolderAlias`](../imagesfolderalias/) ve[`FontsFolderAlias`](../fontsfolderalias/) sırasıyla özellikler. Ancak, CSS. için ayrı bir özellik yoktur.

`ResourceFolderAlias` daha düşük önceliğe sahiptir[`FontsFolderAlias`](../fontsfolderalias/) ve[`ImagesFolderAlias`](../imagesfolderalias/) Örneğin, her ikisi de`ResourceFolderAlias` ve[`FontsFolderAlias`](../fontsfolderalias/) belirtildiğinde, yazı tiplerinin URI'leri kullanılarak oluşturulacaktır[`FontsFolderAlias`](../fontsfolderalias/) resimlerin ve CSS'nin URI'leri kullanılarak oluşturulacaktır`ResourceFolderAlias`.

Eğer`ResourceFolderAlias` boş,[`ResourceFolder`](../resourcefolder/) özellik değeri kaynak URI'lerini oluşturmak için kullanılacak .

Eğer`ResourceFolderAlias` '.' (nokta) olarak ayarlandığında, kaynak URI'leri yalnızca dosya adlarını içerecek, herhangi bir yol içermeyecektir.

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
