---
title: StructuredDocumentTag.CalendarType
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Bunun için takvim türünü belirtir SDT . VarsayılanDefault
type: docs
weight: 50
url: /tr/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Bunun için takvim türünü belirtir **SDT** . Varsayılan:Default

```csharp
public SdtCalendarType CalendarType { get; set; }
```

### Notlar

Bu özelliğe erişim yalnızca şunun için işe yarayacaktır:Date SDT türü.

Diğer tüm SDT türleri için istisna meydana gelecektir.

### Örnekler

Yapılandırılmış belge etiketiyle kullanıcıdan tarih girmesinin nasıl isteneceğini gösterir.

```csharp
Document doc = new Document();

// Kullanıcının tarih girmesini isteyen yapılandırılmış bir belge etiketi ekleyin.
// Microsoft Word'de bu öğe "Tarih seçici içerik kontrolü" olarak bilinir.
// Microsoft Word'de bu etiketin sağ ucundaki oka tıkladığımızda,
// tıklanabilir bir takvim şeklinde bir açılır pencere göreceğiz.
// Etiketin görüntüleyeceği tarihi seçmek için bu açılır pencereyi kullanabiliriz.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Tarihi Suudi Arabistan Arapçası yerel ayarına göre görüntüleyin.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Tarihin görüntüleneceği formatı ayarlayın.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Tarihi Hicri takvime göre gösterelim.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Kullanıcı Microsoft Word'de bir tarih seçmeden önce etikette "Tarih girmek için burayı tıklayın." metni görüntülenecektir.
// Etiketin takvimine göre, etiketin varsayılan bir tarihi görüntülemesini sağlamak için "FullDate" özelliğini ayarlayın.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Ayrıca bakınız

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


