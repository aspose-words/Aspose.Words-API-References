---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.RevisionOptions sınıf. Düzenleme işlemi sırasında belge revizyonlarının nasıl ele alınacağını kontrol etmeye olanak tanır C#'da.
type: docs
weight: 3390
url: /tr/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Düzenleme işlemi sırasında belge revizyonlarının nasıl ele alınacağını kontrol etmeye olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Sabit Sayfa Formatına Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokümantasyon makalesi.

```csharp
public class RevisionOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Yorumlar için kullanılacak rengi belirlemeye izin verir. Varsayılan değer:Red . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Silinen içerik için kullanılacak rengi belirlemeye izin verirDeletion . Varsayılan değer:ByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Silinen içeriğe uygulanacak efektin belirtilmesine izin verirDeletion . Varsayılan değer:StrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Eklenen içerik için kullanılacak rengi belirlemeye olanak tanırInsertion . Varsayılan değer:ByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Eklenen içeriğe uygulanacak efekti belirtmeye olanak tanırInsertion . Varsayılan değer:Underline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Revizyon yorumları için ölçü birimlerini belirlemeye olanak tanır. Varsayılan değer:Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | İçeriğin taşındığı alanlar için kullanılacak rengi belirlemeye olanak tanırMoving . Varsayılan değer:ByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirtmeye olanak tanırMoving . Varsayılan değer:DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | İçeriğin taşındığı alanlarda kullanılacak rengi belirlemeye olanak tanırMoving . Varsayılan değer:ByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirtmeye olanak sağlarMoving . Varsayılan değer:DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Biçimlendirme özelliklerinde değişiklik yapılarak içerik için kullanılacak rengi belirtmeye olanak tanırFormatChange Varsayılan değer:NoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Biçimlendirme özelliklerinde değişiklik yapılarak içerik alanlarına yönelik efektin belirlenmesine olanak tanırFormatChange Varsayılan değer:None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Revize edilmiş bilgileri içeren belge satırlarını tanımlayan kenar çubukları için kullanılacak rengi belirlemeye olanak sağlar. Varsayılan değer:Red . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Revizyon çubuklarının oluşturma konumunu alır veya ayarlar. Varsayılan değer:Outside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Revizyon çubuklarının, noktaların genişliğini alır veya ayarlar. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Revizyonların balonlarda oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değer:None . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Revize edilmiş metin yerine orijinal metnin gösterilip gösterilmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Revizyon çubuklarının revize edilmiş içeriği içeren satırların yakınında oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değer:`doğru` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Revizyon metninin özel biçimlendirme işaretlemesiyle işaretlenip işaretlenmeyeceğini belirtmeye izin verin. Varsayılan değer:`doğru` . |

## Örnekler

İşlenmiş bir çıktı belgesindeki düzeltmelerin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşil olarak değiştirin.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Düzenlenen her satırın solunda görünen çubuğu kaldırın.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
