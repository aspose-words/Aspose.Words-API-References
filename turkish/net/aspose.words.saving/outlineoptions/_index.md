---
title: Class OutlineOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.OutlineOptions sınıf. Anahat seçeneklerini belirlemeye izin verir.
type: docs
weight: 5360
url: /tr/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Anahat seçeneklerini belirlemeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class OutlineOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Bireysel yer imlerinin anahat düzeyini belirlemeye olanak tanır. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Belge dışa aktarıldığında eksik anahat düzeylerinin oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Tabloların içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için ana hatlar oluşturulup oluşturulmayacağını belirtir. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Belge anahattında Word yer işaretlerinin görüntüleneceği varsayılan düzeyi belirtir. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Dosya görüntülendiğinde belge anahattında kaç düzeyin genişletilmiş olarak gösterileceğini belirtir. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | belge taslağına kaç düzeyde başlık (Başlık stilleriyle biçimlendirilmiş paragraflar) ekleneceğini belirtir. |

### Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki üstbilgi/altbilgilerdeki yer işaretlerinin işlenmesini gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF'sinde anahat gezinme bölmesini görüntülemek için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Tümünü görüntülemek için "DefaultBookmarksOutlineLevel" özelliğini "1" olarak ayarlayın
// çıktı PDF'sindeki ana hatların ilk düzeyindeki yer imleri.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.None" olarak ayarlayın
// üstbilgi/altbilgi içindeki yer imlerini dışa aktarma.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.First" olarak ayarlayın
// yalnızca ilk bölümün üstbilgi/altbilgilerindeki yer işaretlerini dışa aktarın.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.All" olarak ayarlayarak
// tüm üstbilgilerde/altbilgilerde bulunan yer işaretlerini dışa aktarın.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


