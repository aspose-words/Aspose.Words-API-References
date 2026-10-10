---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria yöntemi"
linktitle: "get_DocumentSplitCriteria"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria yöntemi. Belgenin Html, Epub veya Azw3 formatında kaydedilirken nasıl bölüneceğini belirtir. Varsayılan değer C++'da HTML için None, EPUB ve AZW3 için HeadingParagraph'tır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Belgenin [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) veya [Azw3](../../../aspose.words/saveformat/) formatında kaydedilirken nasıl bölüneceğini belirtir. Varsayılan değer HTML için [None](../../documentsplitcriteria/), EPUB ve AZW3 için [HeadingParagraph](../../documentsplitcriteria/)dır.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Açıklamalar


Normalde bir belgenin HTML olarak tek bir dosyaya kaydedilmesini istersiniz. Ancak bazı durumlarda çıktıyı birkaç daha küçük HTML sayfasına bölmek tercih edilir. HTML formatında kaydederken bu sayfalar ayrı dosyalara veya akışlara yazdırılır. EPUB formatında kaydederken ise ilgili paketlere dahil edilir.

MHTML formatında kaydedilirken bir belge bölünemez.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
