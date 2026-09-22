---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding metodu"
linktitle: "get_Encoding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding metodu. HTML, MHTML veya EPUB olarak dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer C++'da new UTF8Encoding(false) (BOM'suz UTF-8) şeklindedir."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_encoding/
---
## HtmlSaveOptions::get_Encoding method


HTML, MHTML veya EPUB'a dışa aktarılırken kullanılacak kodlamayı belirtir. Varsayılan değer **new UTF8Encoding(false)** (BOM olmadan UTF-8)'dir.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlSaveOptions::get_Encoding() const
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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
