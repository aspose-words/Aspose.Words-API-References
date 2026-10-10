---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode yöntemi"
linktitle: "get_ExportHeadersFootersMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode yöntemi. Başlıkların ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıktısını belirler. Varsayılan değer HTML/MHTML için PerSection ve EPUB için None'dur C++'ta."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Başlıkların ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıktısını belirler. Varsayılan değer HTML/MHTML için [PerSection](../../exportheadersfootersmode/) ve EPUB için [None](../../exportheadersfootersmode/) dir.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Açıklamalar


HTML sayfalama yapmadığı için başlıkları ve altbilgileri anlamlı bir şekilde HTML'ye çıkarmak zordur.

Bu özellik [PerSection](../../exportheadersfootersmode/) olduğunda, Aspose.Words her bölümün başında ve sonunda yalnızca birincil başlıkları ve altbilgileri dışa aktarır.

Bu [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) olduğunda yalnızca ilk birincil başlık ve son birincil altbilgi (öncekine bağlı olanlar dahil) dışa aktarılır.

Bu özelliği [None](../../exportheadersfootersmode/) olarak ayarlayarak başlık ve altbilgi dışa aktarmayı tamamen devre dışı bırakabilirsiniz.

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

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
