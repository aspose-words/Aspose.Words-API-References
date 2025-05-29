---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: .NET için Aspose.Words
description: Belge revizyonlarını etkin bir şekilde yönetmek ve en iyi sonuçları elde etmek için düzen sürecinizi geliştirmek amacıyla Aspose.Words.Layout.RevisionOptions sınıfını keşfedin.
type: docs
weight: 3840
url: /tr/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Düzen süreci sırasında belge revizyonlarının nasıl işleneceğini kontrol etmenizi sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Sabit Sayfa Biçimine Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) belgeleme makalesi.

```csharp
public class RevisionOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Yorumlar için kullanılacak rengi belirtmeye izin verir. Varsayılan değerRed . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Silinen hücreler için kullanılacak rengin belirlenmesine olanak tanırDeletion . Varsayılan değerPink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Silinen içerik için kullanılacak rengin belirtilmesine olanak tanırDeletion . Varsayılan değerByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Silinen içeriğe uygulanacak efektin belirtilmesine olanak tanırDeletion . Varsayılan değerStrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Eklenen hücreler için kullanılacak rengin belirtilmesine olanak tanırInsertion . Varsayılan değerBlue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Eklenen içerik için kullanılacak rengin belirtilmesine olanak tanırInsertion . Varsayılan değerByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Eklenen içeriğe uygulanacak efekti belirtmeye olanak tanırInsertion . Varsayılan değerUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Gözden geçirme yorumları için ölçüm birimlerini belirtmeye olanak tanır. Varsayılan değerCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | İçeriğin taşındığı alanlar için kullanılacak rengin belirlenmesine olanak tanırMoving . Varsayılan değerByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirtmenize olanak tanırMoving . Varsayılan değerDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | İçeriğin taşındığı alanlar için kullanılacak rengin belirlenmesine olanak tanırMoving . Varsayılan değerByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | İçeriğin taşındığı alanlara uygulanacak efekti belirtmeye olanak tanırMoving . Varsayılan değerDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Biçimlendirme özelliklerinde değişiklik yapıldığında içerik için kullanılacak rengin belirtilmesine olanak tanırFormatChange Varsayılan değerNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmeye olanak tanırFormatChange Varsayılan değerNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Gözden geçirilmiş bilgileri içeren belge satırlarını tanımlayan kenar çubukları için kullanılacak rengi belirtmeye olanak tanır. Varsayılan değerRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Revizyon çubuklarının işleme konumunu alır veya ayarlar. Varsayılan değerOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Revizyon çubuklarının ve noktaların genişliğini alır veya ayarlar. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Revizyonların balonlarda işlenip işlenmeyeceğini belirtmeye izin verir. Varsayılan değerNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Orijinal metnin düzeltilmiş metin yerine gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Gözden geçirilmiş içerik içeren satırların yakınında gözden geçirme çubuklarının oluşturulup oluşturulmayacağını belirtmeye olanak tanır. Varsayılan değer`doğru` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Revizyon metninin özel biçimlendirme işaretlemesiyle işaretlenip işaretlenmeyeceğini belirtmeye izin verir. Varsayılan değer`doğru` . |

## Örnekler

İşlenmiş bir çıktı belgesindeki revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekle, ardından tüm revizyonların rengini yeşil yap.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Her düzeltilen satırın solunda görünen çubuğu kaldır.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
