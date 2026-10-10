---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias method"
linktitle: "get_ImagesFolderAlias"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias yöntemi. HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 39000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


HTML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini HTML formatında kaydettiğinizde, Aspose.Words belgedeki tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](../get_imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ImagesFolderAlias](./) görüntü URI'lerinin nasıl oluşturulacağını belirtmenizi sağlar.

[ImagesFolderAlias](./) boş bir dize değilse, HTML'ye yazılan görüntü URI'si *ImagesFolderAlias + <image file name>* olacaktır.

[ImagesFolderAlias](./) boş bir dize ise, HTML'ye yazılan görüntü URI'si *ImagesFolder + <image file name>* olacaktır.

[ImagesFolderAlias](./) '.' (nokta) olarak ayarlanırsa, diğer seçeneklerden bağımsız olarak görüntü dosya adı HTML'ye yol olmadan yazılacaktır.

Görüntü URI'lerini oluşturmak için klasör adını belirtmenin alternatif yolu, [ResourceFolderAlias](../get_resourcefolderalias/) kullanmaktır.

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
