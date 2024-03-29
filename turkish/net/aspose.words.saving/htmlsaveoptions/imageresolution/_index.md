---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ImageResolution mülk. HTML MHTML veya EPUBa dışa aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan96 dpi  C#'da.
type: docs
weight: 340
url: /tr/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

HTML, MHTML veya EPUB'a dışa aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan:`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Notlar

Bu özellik, taramalı görüntüleri aşağıdaki durumlarda etkiler:[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) :`doğru` ve raster görüntüler olarak dışa aktarılan efekt meta dosyaları. Cropping veya rotasyon gibi bazı görüntü özellikleri, dönüştürülmüş görüntülerin kaydedilmesini gerektirir ve bu durumda dönüştürülmüş görüntüler, verilen çözünürlükte oluşturulur.

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
