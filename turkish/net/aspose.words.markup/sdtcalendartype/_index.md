---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: .NET için Aspose.Words
description: Daha iyi iş akışı verimliliği için çok yönlü takvim seçenekleriyle Office Açık XML belgelerinizi geliştirmek üzere Aspose.Words.Markup.SdtCalendarType enum'unu keşfedin.
type: docs
weight: 4690
url: /tr/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Takvimlerin hangi türlerini belirtmek için kullanılabileceğini belirtir.[`CalendarType`](../structureddocumenttag/calendartype/) bir Office Açık XML belgesinde.

```csharp
public enum SdtCalendarType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Default | `0` | OOXML'de varsayılan değer olarak kullanılır. EşittirGregorian . |
| Gregorian | `0` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvim uygun dile yerelleştirilmelidir. |
| GregorianArabic | `1` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvimin değerleri Arapça olarak sunulmalıdır. |
| GregorianMeFrench | `2` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvimin değerleri Orta Doğu Fransızcası ile sunulmalıdır. |
| GregorianUs | `3` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvimin değerleri İngilizce olarak sunulmalıdır. |
| GregorianXlitEnglish | `4` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvimin değerleri, İngilizce dizelerinin karşılık gelen Arapça karakterlerle gösterimi olmalıdır (Gregoryen takvimi için İngilizcenin Arapça çevirisi). |
| GregorianXlitFrench | `5` | ISO 8601'de tanımlandığı gibi Gregoryen takviminin kullanılacağını belirtir. Bu takvimin değerleri, Fransızca dizelerinin karşılık gelen Arapça karakterlerle gösterimi olmalıdır (Gregoryen takvimi için Fransızcanın Arapça çevirisi). |
| Hebrew | `6` | Gauss formülünde Fısıh Bayramı için açıklandığı gibi İbrani ay takviminin kullanılacağını belirtir [ALINTI] ve Sözlü Yasanın Tam Yeniden Belirtilmesi (Mişne Tora), |
| Hijri | `7` | Suudi Arabistan Krallığı, İslam İşleri, Vakıflar, Davet ve İrşat Bakanlığı tarafından açıklanan Hicri ay takviminin kullanılacağını belirtir. |
| Japan | `8` | Japon Endüstri Standardı JIS X 0301 tarafından açıklandığı gibi Japon İmparatorluk Dönemi takviminin kullanılacağını belirtir. |
| Korea | `9` | Kore Hukuku Yönetmeliği No. 4'te açıklandığı gibi Kore Tangun Çağı takviminin, kullanılacağını belirtir. |
| None | `10` | Hiçbir takvimin kullanılmaması gerektiğini belirtir. |
| Saka | `11` | Hindistan Takvim Reform Komitesi tarafından tanımlanan Saka Dönemi takviminin, Hint Gök Takvimi ve Denizcilik Takvimi'nin bir parçası olarak kullanılacağını belirtir. |
| Taiwan | `12` | Çin Ulusal Standardı CNS 7648 tarafından tanımlanan Tayvan takviminin kullanılacağını belirtir. |
| Thai | `13` | HM Kral Vajiravudh'un (Rama VI) Kraliyet Gazetesi BE 2456'da (1913 AD) Kraliyet Kararnamesi ve Başbakan Phibunsongkhram'ın (1941 AD) yılı Gregoryen takvimine göre 1 Ocak'ta başlatmak ve sıfır yılını MÖ 543 Gregoryen yılına eşlemek için verdiği kararname ile tanımlanan Tayland takviminin kullanılacağını belirtir. |

## Örnekler

Yapılandırılmış bir belge etiketiyle kullanıcıdan bir tarih girmesinin nasıl isteneceğini gösterir.

```csharp
Document doc = new Document();

// Kullanıcıdan bir tarih girmesini isteyen yapılandırılmış bir belge etiketi ekleyin.
// Microsoft Word'de bu öğeye "Tarih seçici içerik denetimi" adı verilir.
// Microsoft Word'de bu etiketin sağ ucundaki oka tıkladığımızda,
// tıklanabilir takvim şeklinde bir açılır pencere göreceğiz.
// Bu açılır pencereyi kullanarak etiketin göstereceği tarihi seçebiliriz.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Tarihi Suudi Arabistan Arapça yerel ayarlarına göre göster.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Tarihin hangi formatta görüntüleneceğini ayarlayın.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Tarihi Hicri takvime göre göster.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Kullanıcı Microsoft Word'de bir tarih seçmeden önce, etiket "Tarih girmek için buraya tıklayın." metnini görüntüler.
// Etiketin takvimine göre, etiketin varsayılan bir tarih görüntülemesini sağlamak için "FullDate" özelliğini ayarlayın.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
