---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ImagesFolderAlias mülk. Bir HTML belgesine yazılan görüntü URIlerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir C#'da.
type: docs
weight: 370
url: /tr/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Bir HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Notlar

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında Aspose.Words'ün belgeye gömülü tüm görsellerini bağımsız dosyalar olarak kaydetmesi gerekir.[`ImagesFolder`](../imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenize ve`ImagesFolderAlias` , görüntü URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Eğer`ImagesFolderAlias` boş bir dize değilse, HTML'ye yazılan görüntü URI'si şöyle olacaktır:ImagesFolderAlias + &lt;resim dosyası adı&gt;.

Eğer`ImagesFolderAlias` boş bir dize ise, HTML'ye yazılan resim URI'si şöyle olacaktır:ImagesFolder + &lt;resim dosyası adı&gt;.

Eğer`ImagesFolderAlias`ayarlandı '.' (nokta) ise, diğer seçeneklere bakılmaksızın görüntü dosyası adı yol olmadan HTML'ye yazılacaktır.

URIs görüntüsünü oluşturmak için klasörün adını belirtmenin alternatif yolu kullanmaktır[`ResourceFolderAlias`](../resourcefolderalias/).

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
