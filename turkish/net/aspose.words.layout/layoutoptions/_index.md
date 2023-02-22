---
title: Class LayoutOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.LayoutOptions sınıf. Belge yerleşim sürecini kontrol etmeye izin veren seçenekleri barındırır.
type: docs
weight: 3150
url: /tr/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Belge yerleşim sürecini kontrol etmeye izin veren seçenekleri barındırır.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Alır veya ayarlar[`IPageLayoutCallback`](../ipagelayoutcallback/)sayfa düzeni modeli tarafından kullanılan uygulama. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Yorumların oluşturulma şeklini alır veya ayarlar. Varsayılan değerShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Sürekli bir bölüm sayfa numaralandırmayı yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | "Belgeyi düzenlemek için yazıcı metriklerini kullan" uyumluluk seçeneğinin yoksayılıp yok sayılmadığının göstergesini alır veya ayarlar. Varsayılan Değer Doğru'dur. |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Revizyon seçeneklerini alır. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Belgedeki gizli metnin işlenip işlenmediğinin göstergesini alır veya ayarlar. Varsayılan Yanlış'tır. |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Paragraf işaretlerinin oluşturulup oluşturulmadığının göstergesini alır veya ayarlar. Varsayılan, False'dır. |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Alır veya ayarlar[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) Gelişmiş Tipografi oluşturma özellikleri için kullanılan uygulama. |

### Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`LayoutOptions`](../../aspose.words/document/layoutoptions/)bu belge için düzen seçeneklerine erişim özelliği.

Bu sınıfta bulunan seçeneklerden herhangi birini değiştirdikten sonra,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Değiştirilen seçeneklerin mizanpaja uygulanabilmesi için method çağrılmalıdır.

### Örnekler

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
// Bazı paragraflar ekleyin, ardından paragrafların sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluşturduğumuzda bir pilcrow (¶) sembolü ile.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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


