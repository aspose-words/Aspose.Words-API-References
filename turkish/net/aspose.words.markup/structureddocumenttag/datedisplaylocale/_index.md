---
title: StructuredDocumentTag.DateDisplayLocale
linktitle: DateDisplayLocale
articleTitle: DateDisplayLocale
second_title: .NET için Aspose.Words
description: StructuredDocumentTag DateDisplayLocale özelliğiyle tarih biçimlerini özelleştirin. Tercih edilen dil biçimlerini zahmetsizce ayarlayarak kullanıcı deneyimini geliştirin.
type: docs
weight: 100
url: /tr/net/aspose.words.markup/structureddocumenttag/datedisplaylocale/
---
## StructuredDocumentTag.DateDisplayLocale property

Bu ekranda görüntülenen tarih için dil biçimini ayarlamayı/almayı sağlar.**SDT** .

```csharp
public int DateDisplayLocale { get; set; }
```

## Notlar

Bu özelliğe erişim yalnızca şu amaçlar için çalışacaktır:Date SDT türü.

Diğer tüm SDT tipleri için istisna oluşacaktır.

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

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
