---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages yöntemi. Bağlantılı görüntülerin URL'si olarak orijinal URL'nin kullanılıp kullanılmayacağını belirtir. C++'da varsayılan değer false'tur."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Orijinal URL'nin bağlantılı görsellerin URL'si olarak kullanılıp kullanılmayacağını belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Açıklamalar


Değer **true** olarak ayarlanırsa [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) değeri, bağlantılı görüntülerin URL'si olarak kullanılır ve bağlantılı görüntüler belge klasörüne veya [ImagesFolder](../get_imagesfolder/) klasörüne yüklenmez.

Değer **false** olarak ayarlanırsa bağlantılı görüntüler belge klasörüne veya [ImagesFolder](../get_imagesfolder/) klasörüne yüklenir ve her bir bağlantılı görüntünün URL'si, belgenin klasörüne, [ImagesFolder](../get_imagesfolder/) ve [ImagesFolderAlias](../get_imagesfolderalias/) özelliklerine bağlı olarak oluşturulur.

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
