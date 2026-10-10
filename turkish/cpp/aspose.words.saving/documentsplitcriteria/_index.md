---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Belgenin C++'da Html, Epub veya Azw3 formatında kaydedilirken parçalara nasıl bölündüğünü belirtir."
type: docs
weight: 52000
url: /tr/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Belgenin [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) veya [Azw3](../../aspose.words/saveformat/) formatında kaydedilirken parçalara nasıl bölündüğünü belirtir.

```cpp
enum class DocumentSplitCriteria
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Belge bölünmez. |
| PageBreak | 1 | Belge, açık sayfa sonlarında parçalara bölünür. Sayfa sonu, bir [PageBreak](../../aspose.words/controlchar/pagebreak/) karakteri, yeni bir sayfada yeni bölümün başlangıcını belirten bir bölüm sonu veya [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) özelliği **true** olarak ayarlanmış bir paragraf ile belirtilebilir. |
| ColumnBreak | 2 | Belge, sütun sonlarında parçalara bölünür. Sütun sonu, bir [ColumnBreak](../../aspose.words/controlchar/columnbreak/) karakteri veya yeni bir sütunda yeni bölümün başlangıcını belirten bir bölüm sonu ile belirtilebilir. |
| SectionBreak | 4 | Belge, herhangi bir türdeki bölüm sonunda parçalara bölünür. |
| HeadingParagraph | 8 | Belge, **Heading 1**, **Heading 2** vb. başlık stilinde biçimlendirilmiş bir paragrafta parçalara bölünür. Bölünecek başlık seviyelerini (1'den belirtilen seviyeye kadar) belirtmek için [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) ile birlikte kullanın. |

## Açıklamalar


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Farklı kriterler kısmen çakışabilir. Örneğin, **Heading 1** stiline sık sık [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) özelliği verilir, bu da iki kritere ( [PageBreak](./) ve [HeadingParagraph](./) ) uymasına neden olur. Bazı bölüm sonları sayfa sonlarına yol açabilir vb. Tipik durumlarda yalnız bir bayrak belirtmek en pratik seçenektir.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
