---
title: "Aspose::Words::Markup::SdtDateStorageFormat enum"
linktitle: "SdtDateStorageFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. SDT bir XML düğümüne C++'ta belgenin veri deposunda bağlandığında tarih SDT'sinin tarihinin nasıl saklandığını/geri alındığını belirtir."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


SDT bir XML düğümüne bağlandığında tarih SDT'sinin tarihinin nasıl saklandığını/geri alındığını belirtir.

```cpp
enum class SdtDateStorageFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Tarih | 0 | Bir tarih SDT'sinin tarih değeri, standart XML Şema Tarih formatında tarih olarak saklanır. |
| DateTime | 1 | Bir tarih SDT'sinin tarih değeri, standart XML Şema TarihSaat formatında tarih olarak saklanır. |
| Metin | 2 | Bir tarih SDT'sinin tarih değeri metin olarak saklanır. |
| Default | n/a | Varsayılan olarak [DateTime](./) kullanılır. |


## Örnekler



Kullanıcıyı yapılandırılmış bir belge etiketiyle tarih girmeye yönlendirmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Kullanıcıyı tarih girmeye yönlendiren bir yapılandırılmış belge etiketi ekleyin.
// Microsoft Word'de bu öğe "Date picker content control" olarak bilinir.
// Microsoft Word'de bu etiketin sağ ucundaki oka tıkladığımızda,
// Tıklanabilir bir takvim şeklinde bir açılır pencere göreceğiz.
// Etiketin göstereceği bir tarihi seçmek için o açılır pencereyi kullanabiliriz.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Tarihi, Suudi Arabistan Arapça yerel ayarına göre görüntüleyin.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Tarihi görüntülemek için kullanılacak formatı ayarlayın.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Tarihi Hicri takvime göre görüntüleyin.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Kullanıcı Microsoft Word'de bir tarih seçmeden önce, etiket "Tarih girmek için buraya tıklayın." metnini gösterecek.
// Etiketin takvimine göre, etiketin varsayılan bir tarih göstermesini sağlamak için "FullDate" özelliğini ayarlayın.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
