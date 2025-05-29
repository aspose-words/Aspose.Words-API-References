---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: .NET için Aspose.Words
description: Aspose.Words.Markup.SdtDateStorageFormat'ın SDT'lerde tarih işlemeyi nasıl geliştirdiğini ve belgelerinizde sorunsuz XML veri entegrasyonunu nasıl sağladığını keşfedin.
type: docs
weight: 4700
url: /tr/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

SDT belgenin veri deposundaki bir XML düğümüne bağlandığında, bir tarih SDT'sinin tarihinin nasıl saklanacağını/alınacağını belirtir.

```csharp
public enum SdtDateStorageFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Date | `0` | Bir tarih SDT'si için tarih değeri, standart XML Şeması Tarih biçiminde bir tarih olarak saklanır. |
| DateTime | `1` | Bir tarih SDT için tarih değeri, standart XML Şeması DateTime biçiminde bir tarih olarak saklanır. |
| Text | `2` | Bir tarih SDT'si için tarih değeri metin olarak saklanır. |
| Default | `1` | Varsayılan olarakDateTime |

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
