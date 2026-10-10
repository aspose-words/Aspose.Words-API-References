---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metodu"
linktitle: "get_FontsFolderAlias"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metodu. HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 34000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


HTML belgesine yazılan yazı tipi URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini HTML formatında kaydettiğinizde ve [ExportFontResources](../get_exportfontresources/) **true** olarak ayarlandığında, Aspose.Words belgedeki kullanılan yazı tiplerini bağımsız dosyalar olarak kaydetmek zorundadır. [FontsFolder](../get_fontsfolder/) yazı tiplerinin nereye kaydedileceğini belirtmenizi sağlar ve [FontsFolderAlias](./) yazı tipi URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Eğer [FontsFolderAlias](./) boş bir dize değilse, HTML'ye yazılan yazı tipi URI'si *FontsFolderAlias + <font file name>* olacaktır.

Eğer [FontsFolderAlias](./) boş bir dize ise, HTML'ye yazılan yazı tipi URI'si *FontsFolder + <font file name>* olacaktır.

Eğer [FontsFolderAlias](./) '.' (nokta) olarak ayarlanırsa, diğer seçeneklerden bağımsız olarak yazı tipi dosya adı HTML'ye yol olmadan yazılacaktır.

Yazı tipi URI'lerini oluşturmak için klasör adını belirtmenin alternatif yolu, [ResourceFolderAlias](../get_resourcefolderalias/) kullanmaktır.

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
