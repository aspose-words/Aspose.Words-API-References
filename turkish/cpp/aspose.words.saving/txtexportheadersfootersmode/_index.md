---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum"
linktitle: "TxtExportHeadersFootersMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum. Başlıkların ve altbilgilerin C++'ta düz metin formatına nasıl aktarıldığını belirtir."
type: docs
weight: 86000
url: /tr/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


Üstbilgi ve altbilgilerin düz metin formatına nasıl dışa aktarılacağını belirtir.

```cpp
enum class TxtExportHeadersFootersMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Başlıklar ve altbilgiler dışa aktarılmaz. |
| PrimaryOnly | 1 | Yalnızca birincil başlıklar ve altbilgiler her bölümün başında ve sonunda dışa aktarılır. |
| AllAtEnd | 2 | Tüm başlıklar ve altbilgiler, belgenin en sonunda, tüm bölüm gövdelerinden sonra yer alır. |


## Örnekler



Başlıkların ve altbilgilerin düz metin formatına nasıl dışa aktarılacağını belirtmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Belgeye çift ve birincil başlık/altbilgileri ekleyin.
// Birincil başlık/altbilgiler, çift başlık/altbilgilerin üzerine yazacaktır.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Bu başlık ve altbilgileri göstermek için sayfalar ekleyin.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.None" olarak ayarlayın
// herhangi bir başlık/altbilgi dışa aktarılmaması için.
// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.PrimaryOnly" olarak ayarlayın
// yalnızca birincil başlık/altbilgi dışa aktarılması için.
// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.AllAtEnd" olarak ayarlayın
// tüm bölüm gövdeleri için tüm başlık ve altbilgileri belgenin sonuna yerleştirmek için.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
