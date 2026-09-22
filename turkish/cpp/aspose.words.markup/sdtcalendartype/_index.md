---
title: "Aspose::Words::Markup::SdtCalendarType enum"
linktitle: "SdtCalendarType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SdtCalendarType enum. Olası takvim türlerini belirtir; bu takvimler C++'da bir Office Open XML belgesinde CalendarType'ı belirtmek için kullanılabilir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Bir Office Open XML belgesinde [CalendarType](../structureddocumenttag/get_calendartype/) belirtmek için kullanılabilecek olası takvim türlerini belirtir.

```cpp
enum class SdtCalendarType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Default | 0 | OOXML'de varsayılan değer olarak kullanılır. [Gregorian](./) eşittir. |
| Gregorian | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim uygun dile yerelleştirilmeli. |
| GregorianArabic | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim için değerler Arapça olarak sunulmalıdır. |
| GregorianMeFrench | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim için değerler Orta Doğu Fransızcası olarak sunulmalıdır. |
| GregorianUs | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim için değerler İngilizce olarak sunulmalıdır. |
| GregorianXlitEnglish | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim için değerler, İngilizce dizelerin ilgili Arapça karakterlerle temsili olmalıdır (Gregoryen takvimi için İngilizce'nin Arapça transliterasyonu). |
| GregorianXlitFrench | n/a | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim için değerler, Fransızca dizelerin ilgili Arapça karakterlerle temsili olmalıdır (Gregoryen takvimi için Fransızca'nın Arapça transliterasyonu). |
| Hebrew | n/a | Gauss formülüyle Passover [CITATION] ve The Complete Restatement of Oral Law (Mishneh Torah) tarafından tanımlanan İbranice luner takviminin kullanılacağını belirtir. |
| Hijri | n/a | Suudi Arabistan Krallığı, İslam İşleri, Vakıflar, Da‘wah ve Rehberlik Bakanlığı tarafından tanımlanan Hicri luner takviminin kullanılacağını belirtir. |
| Japan | n/a | Japon Endüstri Standardı JIS X 0301 tarafından tanımlanan Japon İmparatorluk Dönemi takviminin kullanılacağını belirtir. |
| Kore | n/a | Kore Yasası No. 4'te tanımlanan Kore Tangun Dönemi takviminin kullanılacağını belirtir. |
| None | n/a | Hiçbir takvim kullanılmaması gerektiğini belirtir. |
| Saka | n/a | Hindistan Takvim Reform Komitesi tarafından, Hint Ephemeris ve Denizcilik Takvimi'nin bir parçası olarak tanımlanan Saka Dönemi takviminin kullanılacağını belirtir. |
| Tayvan | n/a | Çin Ulusal Standardı CNS 7648 tarafından tanımlanan Tayvan takviminin kullanılacağını belirtir. |
| Tayca | n/a | H.M. King Vajiravudh (Rama VI) tarafından Kraliyet Gazetesi B. E. 2456 (1913 A.D.) tarihli Kraliyet Kararnamesi ve Başbakan Phibunsongkhram (1941 A.D.) kararnamesi ile yılın Gregoryen 1 Ocak'ta başlamasını ve sıfır yılının Gregoryen 543 B.C. yılına eşlenmesini öngören Tayland takviminin kullanılacağını belirtir. |


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
