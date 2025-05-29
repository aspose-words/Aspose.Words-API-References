---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: .NET için Aspose.Words
description: HTML belgelerinizdeki yazı tipi URI'lerini özelleştirmek için HtmlSaveOptions FontsFolderAlias özelliğini keşfedin. Web tasarımınızı kolaylıkla geliştirin!
type: docs
weight: 320
url: /tr/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Bir HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir.

```csharp
public string FontsFolderAlias { get; set; }
```

## Notlar

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında ve[`ExportFontResources`](../exportfontresources/) olarak ayarlandı`doğru` , Aspose.Words'ün belgede kullanılan yazı tiplerini bağımsız dosyalar olarak kaydetmesi gerekiyor. [`FontsFolder`](../fontsfolder/) yazı tiplerinin nereye kaydedileceğini belirtmenize olanak tanır ve `FontsFolderAlias` yazı tipi URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Eğer`FontsFolderAlias` boş bir dize değilse, HTML'ye yazılan yazı tipi URI'si şu şekilde olacaktır:FontsFolderAlias + &lt;yazı tipi dosya adı&gt;.

Eğer`FontsFolderAlias` boş bir dize ise, HTML'ye yazılan yazı tipi URI'si şu şekilde olacaktırFontsFolder + &lt;font dosya adı&gt;.

Eğer`FontsFolderAlias`'.' (nokta) olarak ayarlanırsa, font dosyası name diğer seçeneklerden bağımsız olarak yol olmaksızın HTML'ye yazılır.

Font URIs 'yi oluşturmak için klasörün adını belirtmenin alternatif yolu şudur:[`ResourceFolderAlias`](../resourcefolderalias/).

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
