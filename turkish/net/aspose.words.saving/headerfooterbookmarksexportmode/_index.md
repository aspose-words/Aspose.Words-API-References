---
title: Enum HeaderFooterBookmarksExportMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode Sıralama. Üstbilgilerdeki/altbilgilerdeki yer imlerinin nasıl dışa aktarılacağını belirtir.
type: docs
weight: 4790
url: /tr/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Üstbilgilerdeki/altbilgilerdeki yer imlerinin nasıl dışa aktarılacağını belirtir.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Üstbilgilerdeki/altbilgilerdeki yer işaretleri dışa aktarılmaz. |
| First | `1` | Yalnızca bölümün ilk üstbilgi/altbilgisindeki yer imi dışa aktarılır. |
| All | `2` | Tüm üstbilgilerdeki/altbilgilerdeki yer işaretleri dışa aktarılır. |

### Örnekler

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


