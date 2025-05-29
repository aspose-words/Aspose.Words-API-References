---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: .NET için Aspose.Words
description: Belge düzeni denetimini optimize etmek ve esnek özelleştirme seçenekleriyle Word işleme deneyiminizi geliştirmek için Aspose.Words.Layout.LayoutOptions'ı keşfedin.
type: docs
weight: 3800
url: /tr/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Belge düzeni sürecini kontrol etmeye izin veren seçenekleri barındırır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Sabit Sayfa Biçimine Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) belgeleme makalesi.

```csharp
public class LayoutOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Alır veya ayarlar[`IPageLayoutCallback`](../ipagelayoutcallback/) sayfa düzeni modeli tarafından kullanılan uygulama. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Yorumların işlenme şeklini alır veya ayarlar. Varsayılan değerShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Sürekli bir bölüm sayfa numaralandırmasını yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | "Belgeyi düzenlemek için yazıcı ölçümlerini kullan" uyumluluk seçeneğinin göz ardı edilip edilmediğine ilişkin göstergeyi alır veya ayarlar. Varsayılan`doğru` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Yazı tipi değişiminden sonra orijinal yazı tipi ölçümlerinin kullanılıp kullanılmayacağına dair bir gösterge alır veya ayarlar. Varsayılan`doğru` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Revizyon seçeneklerini alır. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Belgedeki gizli metnin işlenip işlenmediğine ilişkin göstergeyi alır veya ayarlar. Varsayılan`YANLIŞ` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Paragraf işaretlerinin işlenip işlenmediğine dair göstergeyi alır veya ayarlar. Varsayılan`YANLIŞ` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Alır veya ayarlar[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Gelişmiş Tipografi oluşturma özellikleri için kullanılan uygulama. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız.[`LayoutOptions`](../../aspose.words/document/layoutoptions/) Bu belge için düzen seçeneklerine erişim özelliği.

Bu sınıftaki seçeneklerden herhangi birini değiştirdikten sonra,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Değiştirilen seçeneklerin düzene uygulanabilmesi için method çağrılmalıdır.

## Örnekler

İşlenmiş çıktı belgesinde metnin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Gizli metin ekleyin, ardından işlenmiş belgeden bunu çıkarmak isteyip istemediğimizi belirtin.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

İşlenmiş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Birkaç paragraf ekleyin, ardından paragraf sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluştururken pilcrow (¶) sembolüyle.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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
