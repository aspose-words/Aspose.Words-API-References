---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: .NET için Aspose.Words
description: PdfSaveOptions HeaderFooterBookmarksExportMode özelliğinin gelişmiş PDF işlevselliği için üstbilgilerde ve altbilgilerde yer imi dışa aktarımını nasıl iyileştirdiğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

Başlıklar/altbilgilerdeki yer imlerinin nasıl dışa aktarılacağını belirler.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## Notlar

Varsayılan değer:All.

Bu özellik, aşağıdakilerle birlikte kullanılır:[`OutlineOptions`](../outlineoptions/) seçenek.

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

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
