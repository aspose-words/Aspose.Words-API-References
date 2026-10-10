---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metodu"
linktitle: "get_FontsFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metodu. Bir belge HTML'ye dışa aktarılırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 33000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Bir belge HTML olarak dışa aktarıldığında yazı tiplerinin kaydedileceği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini HTML formatında kaydettiğinizde ve [ExportFontResources](../get_exportfontresources/) **true** olarak ayarlandığında, Aspose.Words belgedeki kullanılan yazı tiplerini bağımsız dosyalar olarak kaydetmek zorundadır. [FontsFolder](./) yazı tiplerinin nereye kaydedileceğini belirtmenizi sağlar ve [FontsFolderAlias](../get_fontsfolderalias/) yazı tipi URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak yazı tiplerini belgenin kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [FontsFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words yazı tiplerini kaydedecek bir klasöre sahip olmaz, ancak yine de bir yerde yazı tiplerini kaydetmesi gerekir. Bu durumda, [FontsFolder](./) özelliğinde erişilebilir bir klasör belirtmeniz veya [FontSavingCallback](../get_fontsavingcallback/) olay işleyicisi aracılığıyla özel akışlar sağlamanız gerekir.

Eğer [FontsFolder](./) tarafından belirtilen klasör mevcut değilse, otomatik olarak oluşturulacaktır.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
