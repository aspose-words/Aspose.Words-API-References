---
title: Enum PdfPageMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfPageMode Sıralama. PDF okuyucuda açıldığında PDF belgesinin nasıl görüntüleneceğini belirtir.
type: docs
weight: 5220
url: /tr/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

PDF okuyucuda açıldığında PDF belgesinin nasıl görüntüleneceğini belirtir.

```csharp
public enum PdfPageMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseNone | `0` | Ne belge taslağı ne de küçük resimler görünür değil. |
| UseOutlines | `1` | Belge anahattı görünür. PDF belgesinde anahat yoksa, anahat gezinme bölmesinin yine de görünmeyeceğini unutmayın. |
| UseThumbs | `2` | Küçük resimler görülebilir. |
| FullScreen | `3` | Menü çubuğu, pencere kontrolleri veya başka herhangi bir pencerenin görünmediği tam ekran modu. |
| UseOC | `4` | İsteğe bağlı içerik grubu paneli görünür. |
| UseAttachments | `5` | Ekler paneli görünür. |

### Örnekler

Bir çıktı belgesini açarken bazı PDF okuyucularının izlemesi gereken talimatların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// PDF okuyucunun kaydedilen dosyayı açmasını sağlamak için "PageMode" özelliğini "PdfPageMode.FullScreen" olarak ayarlayın
// monitörün görüntüsünü devralan ve görünür hiçbir denetimi olmayan tam ekran modunda belge.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseThumbs" olarak ayarlayın
// belgedeki her sayfa için bir küçük resim ile.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseOC" olarak ayarlayın
// bu, belgede bulunan herhangi bir katmanla çalışmamıza izin verir.
// PDF okuyucuyu almak için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın
// mümkünse taslağı da görüntülemek için.
// PDF okuyucunun yalnızca belgenin kendisini görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseNone" olarak ayarlayın.
// Ekler panelini görünür kılmak için "PageMode" özelliğini "PdfPageMode.UseAttachments" olarak ayarlayın.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

PDF'ye dönüştürdüğümüz bir belgedeki üstbilgi/altbilgilerdeki yer imlerini işlemek için gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF'sinde anahat gezinme bölmesini görüntülemek için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Tümünü görüntülemek için "DefaultBookmarksOutlineLevel" özelliğini "1" olarak ayarlayın
// çıktı PDF'sindeki anahattın ilk seviyesindeki yer imleri.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.None" olarak ayarlayın.
// üstbilgiler/altbilgiler içindeki yer işaretlerini dışa aktarmayın.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.First" olarak ayarlayın.
// yalnızca ilk bölümün üstbilgi/altbilgilerindeki yer işaretlerini dışa aktarın.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.All" olarak ayarlayın.
// tüm üstbilgilerde/altbilgilerde bulunan yer imlerini dışa aktarın.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


