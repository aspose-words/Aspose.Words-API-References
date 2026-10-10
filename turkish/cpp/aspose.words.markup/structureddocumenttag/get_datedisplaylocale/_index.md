---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale metodu"
linktitle: "get_DateDisplayLocale"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale metodu. C++ içinde bu SDT'de görüntülenen tarihin dil formatını ayarlamaya/almaya izin verir."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_datedisplaylocale/
---
## StructuredDocumentTag::get_DateDisplayLocale method


Bu **SDT** içinde görüntülenen tarihin dil biçimini ayarlamaya/alma izni verir.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale()
```

## Açıklamalar


Bu özelliğe erişim yalnızca [Date](../../sdttype/) SDT türü için çalışır.

Diğer tüm SDT türleri için bir istisna oluşacaktır.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
