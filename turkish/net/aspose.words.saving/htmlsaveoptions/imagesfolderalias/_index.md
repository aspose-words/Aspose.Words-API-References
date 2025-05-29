---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: .NET için Aspose.Words
description: HTML belgelerinizdeki resim URI'lerini kolayca yönetmek için HtmlSaveOptions ImagesFolderAlias özelliğini keşfedin. Bu temel özellik ile iş akışınızı basitleştirin!
type: docs
weight: 370
url: /tr/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Bir HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Notlar

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında, Aspose.Words'ün belgeye gömülü tüm resimleri bağımsız dosyalar olarak kaydetmesi gerekir.[`ImagesFolder`](../imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenize olanak tanır ve`ImagesFolderAlias` görüntü URI'lerinin nasıl oluşturulacağını belirtmeye izin verir.

Eğer`ImagesFolderAlias` boş bir dize değilse, HTML'ye yazılan resim URI'si şu şekilde olacaktır:ImagesFolderAlias + &lt;resim dosya adı&gt;.

Eğer`ImagesFolderAlias`boş bir dize ise, HTML'ye yazılan resim URI'si şu şekilde olacaktırImagesFolder + &lt;resim dosya adı&gt;.

Eğer`ImagesFolderAlias` '.' (nokta) olarak ayarlanırsa, resim dosyası adı diğer seçeneklerden bağımsız olarak yol olmaksızın HTML'ye yazılır.

Görüntü URIs oluşturmak için klasörün adını belirtmenin alternatif yolu, şunu kullanmaktır:[`ResourceFolderAlias`](../resourcefolderalias/).

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
