---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ile görüntü çözünürlüğünü zahmetsizce ayarlayın. Çarpıcı görseller için HTML, MHTML veya EPUB dışa aktarımlarınızı özelleştirilebilir ayarlarla optimize edin.
type: docs
weight: 340
url: /tr/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

HTML, MHTML veya EPUB'a aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Notlar

Bu özellik, raster görüntüleri şu şekilde etkiler:[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) şudur`doğru` ve efekt meta dosyaları raster görüntüler olarak dışa aktarılır. Cropping veya döndürme gibi bazı görüntü özellikleri dönüştürülmüş görüntüleri kaydetmeyi gerektirir ve bu durumda dönüştürülmüş görüntüler given çözünürlükte oluşturulur.

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
