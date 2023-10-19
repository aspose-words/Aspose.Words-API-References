---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words for .NET
description: PdfSaveOptions HeaderFooterBookmarksExportMode mülk. Üstbilgi/altbilgilerdeki yer işaretlerinin nasıl dışa aktarılacağını belirler C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

Üstbilgi/altbilgilerdeki yer işaretlerinin nasıl dışa aktarılacağını belirler.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## Notlar

Varsayılan değer:All.

Bu özellik aşağıdakilerle birlikte kullanılır:[`OutlineOptions`](../outlineoptions/) seçenek.

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

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
