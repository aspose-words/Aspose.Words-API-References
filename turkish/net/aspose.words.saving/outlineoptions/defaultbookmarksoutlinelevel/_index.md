---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: .NET için Aspose.Words
description: DefaultBookmarksOutlineLevel özelliğinin, anahattaki yer imi görünürlüğünü optimize ederek Word belgelerinizi nasıl geliştirdiğini keşfedin. Bugün üretkenliği artırın!
type: docs
weight: 50
url: /tr/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Word yer imlerinin görüntüleneceği belge anahattındaki varsayılan düzeyi belirtir.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Notlar

Bireysel yer imleri düzeyi, şunu kullanarak belirtilebilir:[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) mülk.

belirtin ve Word yer imleri belge taslağında görüntülenmeyecektir. 1 belirtin ve Word yer imleri belge taslağında 1. düzeyde görüntülenecektir; 2 belirtin 2. düzey için vb.

Varsayılan 0'dır. Geçerli aralık 0 ila 9'dur.

## Örnekler

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

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
