---
title: Class RevisionOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.RevisionOptions sınıf. Düzen işlemi sırasında belge revizyonlarının nasıl işlendiğini kontrol etmeye izin verir.
type: docs
weight: 3190
url: /tr/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Düzen işlemi sırasında belge revizyonlarının nasıl işlendiğini kontrol etmeye izin verir.

```csharp
public class RevisionOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Yorumlar için kullanılacak rengi belirlemeye izin verir. Varsayılan değerRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Silinen içerik için kullanılacak rengi belirlemeye izin verirDeletion . Varsayılan değerByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Silinen içeriğe uygulanacak efekti belirlemeye izin verirDeletion . Varsayılan değerStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Eklenen içerik için kullanılacak rengi belirlemeye izin verirInsertion . Varsayılan değerByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Eklenen içeriğe uygulanacak efekti belirlemeye izin verirInsertion . Varsayılan değerUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Revizyon yorumları için ölçü birimlerini belirlemeye izin verir. Varsayılan değerCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | İçeriğin taşındığı alanlar için kullanılacak rengi belirlemeye izin verirMoving . Varsayılan değerByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirlemeye izin verirMoving . Varsayılan değerDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | İçeriğin taşındığı alanlar için kullanılacak rengi belirlemenizi sağlarMoving . Varsayılan değerByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirlemenizi sağlarMoving . Varsayılan değerDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Biçimlendirme özelliklerinde değişiklik yapılan içerik için kullanılacak rengi belirlemeye izin verirFormatChange Varsayılan değerNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Biçimlendirme özelliklerinde değişiklik yapılan içerik alanları için efekt belirlemeye izin verirFormatChange Varsayılan değerNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Gözden geçirilmiş bilgi içeren belge satırlarını tanımlayan kenar çubukları için kullanılacak rengi belirlemeye izin verir. Varsayılan değerRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Revizyon çubuklarının oluşturma konumunu alır veya ayarlar. Varsayılan değerOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Revizyon çubuklarının, noktaların genişliğini alır veya ayarlar. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Revizyonların balonlarda oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değerNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Düzeltilmiş metin yerine orijinal metnin gösterilip gösterilmeyeceğini belirlemeye izin verir. Varsayılan değer False'dır. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Düzeltme çubuklarının, gözden geçirilmiş içerik içeren satırların yakınında oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değer True'dur. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Revizyon metninin özel biçimlendirme işaretlemesiyle işaretlenip işaretlenmeyeceğini belirlemeye izin verin. Varsayılan değer True'dur. |

### Örnekler

İşlenmiş bir çıktı belgesindeki revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşil olarak değiştirin.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Revize edilen her satırın solunda görünen çubuğu kaldırın.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)


