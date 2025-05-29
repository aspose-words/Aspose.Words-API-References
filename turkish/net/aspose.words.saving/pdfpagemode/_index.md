---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: .NET için Aspose.Words
description: Özelleştirilebilir PDF görüntüleme seçenekleri için Aspose.Words.PdfPageMode enum'unu keşfedin ve herhangi bir PDF okuyucuda kullanıcı deneyimini geliştirin. Belgelerinizi bugün optimize edin!
type: docs
weight: 6300
url: /tr/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

PDF belgesinin PDF okuyucuda açıldığında nasıl görüntüleneceğini belirtir.

```csharp
public enum PdfPageMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseNone | `0` | Ne belge ana hatları ne de küçük resim görüntüleri görünür. |
| UseOutlines | `1` | Belgenin ana hatları görünür. PDF belgesinde ana hatlar yoksa ana hat gezinme bölmesinin yine de görünür olmayacağını unutmayın. |
| UseThumbs | `2` | Küçük resim görüntüleri görünüyor. |
| FullScreen | `3` | Menü çubuğu, pencere kontrolleri veya başka herhangi bir pencerenin görünmediği tam ekran modu. |
| UseOC | `4` | İsteğe bağlı içerik grubu paneli görünür. |
| UseAttachments | `5` | Ekler paneli görünür. |

## Örnekler

Bazı PDF okuyucularının çıktı belgesini açarken izlemesi gereken talimatların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// PDF okuyucunun kaydedilen dosyayı açmasını sağlamak için "PageMode" özelliğini "PdfPageMode.FullScreen" olarak ayarlayın
// Monitörün ekranını kaplayan ve hiçbir kontrolün görünmediği tam ekran modundaki belge.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseThumbs" olarak ayarlayın
// belgedeki her sayfa için bir küçük resim ile.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseOC" olarak ayarlayın
// Bu, belgede bulunan tüm katmanlarla çalışmamıza olanak tanır.
// PDF okuyucusunu almak için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın
// mümkünse ana hatları da görüntülemek için.
// PDF okuyucunun yalnızca belgenin kendisini görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseNone" olarak ayarlayın.
// Ekler panelini görünür kılmak için "PageMode" özelliğini "PdfPageMode.UseAttachments" olarak ayarlayın.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

PDF'e dönüştürdüğümüz bir belgedeki başlık/altbilgilerdeki yer imlerinin nasıl işleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıkış PDF'inde anahat gezinme bölmesini görüntülemek için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Tümünü görüntülemek için "DefaultBookmarksOutlineLevel" özelliğini "1" olarak ayarlayın
// çıktı PDF'indeki anahattın ilk seviyesindeki yer imleri.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.None" olarak ayarlayın
// Başlıklar/altbilgiler içinde bulunan hiçbir yer imini dışa aktarmayın.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.First" olarak ayarlayın
// sadece ilk bölümün üstbilgi/altbilgilerindeki yer imlerini dışa aktar.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.All" olarak ayarlayın
// tüm başlıklarda/altbilgilerde bulunan yer imlerini dışa aktar.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
