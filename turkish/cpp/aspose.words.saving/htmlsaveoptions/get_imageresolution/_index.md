---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution method"
linktitle: "get_ImageResolution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution yöntemi. Görüntüleri HTML, MHTML veya EPUB olarak dışa aktarırken çıkış çözünürlüğünü belirtir. C++'da varsayılan değer %96 dpi'dir."
type: docs
weight: 36000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


HTML, MHTML veya EPUB olarak dışa aktarırken görüntüler için çıkış çözünürlüğünü belirtir. Varsayılan değer **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Açıklamalar


Bu özellik, [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) **true** olduğunda raster görüntüleri etkiler ve raster görüntü olarak dışa aktarılan metafilleri etkiler. Kırpma veya döndürme gibi bazı görüntü özellikleri dönüştürülmüş görüntülerin kaydedilmesini gerektirir ve bu durumda dönüştürülmüş görüntüler verilen çözünürlükte oluşturulur.

## Örnekler



Aspose.Words'in bir belgeyi HTML olarak kaydederken oluşturacağı harici kaydedilen kaynaklar için klasörleri ve klasör takma adlarını nasıl ayarlayacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
