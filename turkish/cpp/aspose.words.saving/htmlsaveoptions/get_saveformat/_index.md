---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. C++'ta Html, Mhtml, Epub, Azw3 veya Mobi olabilir."
type: docs
weight: 45000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_saveformat/
---
## HtmlSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) veya [Mobi](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat() override
```


## Örnekler



.epub formatında bir belge kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Kaydedeceğimiz bir belgenin kodlamasını belirtmek için bir SaveOptions nesnesi kullanın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Varsayılan olarak, çıkış .epub belgesi tüm içeriğini tek bir HTML bölümünde tutar.
// Bir bölme ölçütü, belgeyi birden fazla HTML bölümüne ayırmamıza olanak tanır.
// Belgeyi başlık paragraflarına bölmek için ölçütleri ayarlayacağız.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için faydalıdır.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
