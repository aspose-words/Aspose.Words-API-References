---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode'un sorunsuz belge yönetimi için üstbilgi ve altbilgilerde yer imi dışa aktarmayı nasıl geliştirdiğini keşfedin.
type: docs
weight: 5800
url: /tr/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Başlıklar/altbilgilerdeki yer imlerinin nasıl dışa aktarılacağını belirtir.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Başlıklar/altbilgilerdeki yer imleri dışa aktarılmaz. |
| First | `1` | Sadece bölümün ilk başlığı/altbilgisindeki yer imi dışa aktarılır. |
| All | `2` | Tüm başlıklar/altbilgilerdeki yer imleri dışa aktarılır. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
