---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.LayoutOptions sınıf. Belge düzeni sürecini kontrol etmeye olanak sağlayan seçenekleri içerir C#'da.
type: docs
weight: 3350
url: /tr/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Belge düzeni sürecini kontrol etmeye olanak sağlayan seçenekleri içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Sabit Sayfa Formatına Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokümantasyon makalesi.

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
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Yorumların oluşturulma şeklini alır veya ayarlar. Varsayılan değer:ShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Sürekli bir bölüm sayfa numaralandırmayı yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | "Belgeyi düzenlemek için yazıcı ölçümlerini kullan" uyumluluk seçeneğinin göz ardı edilip edilmediğine ilişkin göstergeyi alır veya ayarlar. Varsayılan:`doğru` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Yazı tipi değişiminden sonra orijinal yazı tipi ölçümlerinin kullanılıp kullanılmaması gerektiğine ilişkin bir gösterge alır veya ayarlar. Varsayılan:`doğru` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Revizyon seçeneklerini alır. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Belgedeki gizli metnin oluşturulup oluşturulmayacağına ilişkin göstergeyi alır veya ayarlar. Varsayılan:`YANLIŞ` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Paragraf işaretlerinin oluşturulup oluşturulmayacağına ilişkin göstergeyi alır veya ayarlar. Varsayılan:`YANLIŞ` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Alır veya ayarlar[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Gelişmiş Tipografi oluşturma özellikleri için kullanılan uygulama. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`LayoutOptions`](../../aspose.words/document/layoutoptions/) Bu belgenin düzen seçeneklerine erişim özelliği.

Bu sınıfta mevcut seçeneklerden herhangi birini değiştirdikten sonra,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Değiştirilen seçeneklerin düzene uygulanabilmesi için method çağrılmalıdır.

## Örnekler

İşlenmiş bir çıktı belgesindeki metnin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Gizli metni ekleyin, ardından onu işlenmiş bir belgeden çıkarmak isteyip istemediğimizi belirtin.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

İşlenmiş bir çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Birkaç paragraf ekleyin, ardından paragraf sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluşturduğumuzda pilcrow (¶) sembolüyle.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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
