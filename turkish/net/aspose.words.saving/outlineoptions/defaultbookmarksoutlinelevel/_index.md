---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words for .NET
description: OutlineOptions DefaultBookmarksOutlineLevel mülk. Belge anahattında Word yer işaretlerinin görüntüleneceği varsayılan düzeyi belirtir C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Belge anahattında Word yer işaretlerinin görüntüleneceği varsayılan düzeyi belirtir.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Notlar

Bireysel yer imlerinin düzeyi kullanılarak belirtilebilir.[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) mülk.

0 belirtin ve Word yer imleri belge anahattında görüntülenmez. 1 belirtin ve Word yer imleri belge anahattında 1. düzeyde görüntülenecektir; 2. seviye için 2 vb.

Varsayılan 0'dır. Geçerli aralık 0 ila 9'dur.

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

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
