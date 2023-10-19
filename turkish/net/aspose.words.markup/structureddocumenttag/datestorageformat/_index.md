---
title: StructuredDocumentTag.DateStorageFormat
linktitle: DateStorageFormat
articleTitle: DateStorageFormat
second_title: Aspose.Words for .NET
description: StructuredDocumentTag DateStorageFormat mülk. SDTnin saklandığı tarih için tarihin biçimini alır/ayarlar.SDTbelgenin veri deposundaki bir XML düğümüne bağlanır. Varsayılan değerDateTime C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.markup/structureddocumenttag/datestorageformat/
---
## StructuredDocumentTag.DateStorageFormat property

SDT'nin saklandığı tarih için tarihin biçimini alır/ayarlar.**SDT**belgenin veri deposundaki bir XML düğümüne bağlanır. Varsayılan değer:DateTime

```csharp
public SdtDateStorageFormat DateStorageFormat { get; set; }
```

## Notlar

Bu özelliğe erişim yalnızca şunun için işe yarayacaktır:Date SDT türü.

Diğer tüm SDT türleri için istisna meydana gelecektir.

## Örnekler

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

* enum [SdtDateStorageFormat](../../sdtdatestorageformat/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
