---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode Sıralama. Üstbilgi/altbilgilerdeki yer işaretlerinin nasıl dışa aktarılacağını belirtir C#'da.
type: docs
weight: 5050
url: /tr/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Üstbilgi/altbilgilerdeki yer işaretlerinin nasıl dışa aktarılacağını belirtir.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Üstbilgi/altbilgilerdeki yer işaretleri dışa aktarılmaz. |
| First | `1` | Yalnızca bölümün ilk üstbilgi/altbilgisindeki yer imi dışa aktarılır. |
| All | `2` | Tüm üstbilgi/altbilgilerdeki yer işaretleri dışa aktarılır. |

## Örnekler

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
