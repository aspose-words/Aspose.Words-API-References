---
title: "Aspose::Words::Saving::ExportHeadersFootersMode enum'ı"
linktitle: "ExportHeadersFootersMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ExportHeadersFootersMode enum'ı. Başlıkların ve altbilgilerin C++'ta HTML, MHTML veya EPUB formatına nasıl dışa aktarıldığını belirtir."
type: docs
weight: 55000
url: /tr/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Üstbilgi ve altbilgilerin HTML, MHTML veya EPUB'a nasıl dışa aktarılacağını belirtir.

```cpp
enum class ExportHeadersFootersMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Başlıklar ve altbilgiler dışa aktarılmaz. |
| PerSection | 1 | Birincil üstbilgiler ve altbilgiler, her bölümün başında ve sonunda dışa aktarılır. |
| FirstSectionHeaderLastSectionFooter | 2 | İlk bölümün birincil üstbilgisi belgenin başında, birincil altbilgisi ise sonunda dışa aktarılır. |
| FirstPageHeaderFooterPerSection | 3 | İlk sayfa üstbilgisi ve altbilgisi, her bölümün başında ve sonunda dışa aktarılır. |


## Örnekler



Bir belgeyi HTML olarak kaydederken üstbilgi/altbilgileri nasıl atlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Bu belge üstbilgi ve altbilgiler içerir. Onlara "HeadersFooters" koleksiyonu aracılığıyla erişebiliriz.
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// .html gibi formatlar belgeyi sayfalara bölmez, bu yüzden üstbilgi/altbilgiler aynı şekilde çalışmaz
// Microsoft Word kullanarak belgeyi .docx olarak açtığımızda çalışırlardı.
// Üstbilgi/altbilgili bir belgeyi html'ye dönüştürürsek, dönüşüm üstbilgi/altbilgileri gövde metnine dahil eder.
// Html'ye dönüştürürken üstbilgi/altbilgileri atlamak için bir SaveOptions nesnesi kullanabiliriz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Kaydedilmiş belgemizi açın ve üstbilgi metnini içermediğini doğrulayın
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
